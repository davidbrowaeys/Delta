# DeloitteForce-CLI

A cli plugin for the Salesforce CLI built by David Browaeys containing a lot of helpful commands. 

## Pre-requisite
1. Install [SDFX CLI](https://developer.salesforce.com/tools/sfdxcli) 

2. Install [node.js. + npm](https://nodejs.org/en/). 
Once installed, checkout proxy setting if you are behind corporate proxy.

## Install Delta-CLI

1. go to your local workspace and clone DeloitteForce-CLI repository:

  ```shell
  git clone ssh://git@dvcs.deloittedigital.com.au:22/dforce/delta-cli.git
  ``` 


2. Go to DeloitteForce-CLI folder and install it globally using npm: 

  ```shell
  cd delta-cli
  sudo npm install -g .
  ```

  ```shell
  deloitte force:source:delta -r delta -m tags -p mytag
  deloitte force:source:delta -r delta -m commitid -k 123456
  deloitte force:source:delta -r delta -m branch -k origin/master
  ```
Here is an example of how to use the deloitte delta command in a pipeline JenkinsFile
  ```groovy
  def jsonSlurper = new JsonSlurper();
  bat "deloitte force:source:delta -m branch -k master --json -r > delta.json";
  stdout = readFile("delta.json").trim();
  def delta = jsonSlurper.parseText(stdout);
  def options = "";
  if (delta.testClasses != null && delta.testClasses.isEmpty() == false){
      options = "-l RunSpecifiedTest -r "+ delta.testClasses.join(',');
  }
  def cmd = "sfdx force:source:deploy -p "+delta.deltaMeta.join(',')+" -u prod -w 600 "+options;
  bat cmd;
  ```