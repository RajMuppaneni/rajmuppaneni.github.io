# Solr Workspace Setup Windows
##  Prerequisites
1. [Sign up for Github](https://github.com/)
2. Setup [GitHub Desktop](https://help.github.com/articles/set-up-git/) or [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
3. Apache Ant [Install & Setup](http://ant.apache.org/manual/index.html)
4. Setup [Apache Ivy](http://ant.apache.org/ivy/history/latest-milestone/tutorial.html)/[Maven](https://maven.apache.org/install.html)
5. If working from behind a firewall, ensure appropriate proxy settings are in place for Git,Ivy,Maven and Ant.
6. Fork [lucene-solr](https://github.com/apache/lucene-solr/) repository
7. Clone your fork to your file system.
8. Eclipse
9. Java 1.8+

## My Setup
1. Git
2. Apache Ant
3. Apache Ivy
4. Eclipse
5. Java 1.8
6. Windows

## Getting Started
Navigate to your file system with the content from your fork.   

lucene/ is a search engine library  
solr/ is a search engine server that uses lucene    

1. Setup eclipse by running `ant eclipse`. This will generate the required .project,.classpath and .settings  
2. Ensure the initial and max heap set to a higher number in eclipse.ini  
3. Open eclipse and choose the parent of lucene and solr as workspace location. 
4. Import > Existing project into workspace *(be patient as it takes a while to import and build)*  

##  Debuggersville
**Are you puzzled by solr behvior in some case? then this section is for you.**

1.  Right click your lucene-solr project and choose `Debug As > Debug Configurations` 
2.  Under the `Remote Java Application` category. Click New to create a new debug configuration.  
3.  Give it a name your like to use and setup the port that you would like to use for debugging.  
4.  You should now be able to set breakpoints throughout the Solr/Lucene code base, step through code, and do all the other fun stuff you can do. 

##  Running/Debug Solr Examples 
1.  Navigate to /solr directory on your file system 
2.  Open build.xml and find the target for `run-example`, ensure the port you choose to debug on is specified in the `example.jvm.line` property as `address`.
3.  If you are looking to debug set system property `-Dexample.debug=true` to enable JVM debugging. (*java -Dexample.debug=true*)
4.  `ant run-example` *(be patient as it takes a while to reveal its magic)*  
5.  In case you are debugging after you see *Listening for transport dt_socket at address: {port_number}* on the command prompt,switch to eclipse and debug using the configuration we setup earlier.
6.  You can navigate to solr-webapp @ localhost:8983/solr/# 

# Have Fun
