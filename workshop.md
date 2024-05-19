## Download JF CLI:
```https://jfrog.com/getcli/```
### Direct download of jf exe from the JFrog site.
``` https://releases.jfrog.io/artifactory/jfrog-cli/v2-jf/2.56.1/jfrog-cli-windows-amd64/jf.exe ```

## Maven Download:

```
(base) nagag@nagag-mac downloadmvn % pwd
/Users/nagag/work/pkgtypes/maven/maven-example/downloadmvn
(base) nagag@nagag-mac downloadmvn % mvn dependency:get -DgroupId=dom4j -DartifactId=dom4j -Dversion=1.6.1 -Dtransitive=false -s settings.xml
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- dependency:3.6.1:get (default-cli) @ standalone-pom ---
[INFO] Resolving dom4j:dom4j:jar:1.6.1
Downloading from central: https://psemea.jfrog.io/artifactory/maven-virt/dom4j/dom4j/1.6.1/dom4j-1.6.1.jar
Downloading from snapshots: https://psemea.jfrog.io/artifactory/maven-virt/dom4j/dom4j/1.6.1/dom4j-1.6.1.jar
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.500 s
[INFO] Finished at: 2024-05-03T21:48:31+05:30
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:3.6.1:get (default-cli) on project standalone-pom: Couldn't download artifact: The following artifacts could not be resolved: dom4j:dom4j:jar:1.6.1 (absent): Could not transfer artifact dom4j:dom4j:jar:1.6.1 from/to central (https://psemea.jfrog.io/artifactory/maven-virt): status code: 403, reason phrase:  (403) -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException
(base) nagag@nagag-mac downloadmvn %
```

## python download:

```
(base) nagag@nagag-mac download % pwd
/Users/nagag/work/pkgtypes/python/PyYAML/download
(base) nagag@nagag-mac download % jf pip download PyYAML==5.2
21:51:05 [🔵Info] Running pip download
Looking in indexes: https://nagag:****@psemea.jfrog.io/artifactory/api/pypi/pipy-remote/simple
Collecting PyYAML==5.2
  ERROR: HTTP error 403 while getting https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/packages/packages/8d/c9/e5be955a117a1ac548cdd31e37e8fd7b02ce987f9655f5c7563c656d5dcb/PyYAML-5.2.tar.gz#sha256=c0ee8eca2c582d29c3c2ec6e2c4f703d1b7f1fb10bc72317355a746057e7346c (from https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/simple/pyyaml/)
ERROR: Could not install requirement PyYAML==5.2 from https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/packages/packages/8d/c9/e5be955a117a1ac548cdd31e37e8fd7b02ce987f9655f5c7563c656d5dcb/PyYAML-5.2.tar.gz#sha256=c0ee8eca2c582d29c3c2ec6e2c4f703d1b7f1fb10bc72317355a746057e7346c because of HTTP error 403 Client Error:  for url: https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/packages/packages/8d/c9/e5be955a117a1ac548cdd31e37e8fd7b02ce987f9655f5c7563c656d5dcb/PyYAML-5.2.tar.gz for URL https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/packages/packages/8d/c9/e5be955a117a1ac548cdd31e37e8fd7b02ce987f9655f5c7563c656d5dcb/PyYAML-5.2.tar.gz#sha256=c0ee8eca2c582d29c3c2ec6e2c4f703d1b7f1fb10bc72317355a746057e7346c (from https://psemea.jfrog.io/artifactory/api/pypi/pipy-remote/simple/pyyaml/)
21:51:08 [🚨Error] exit status 1
```

## NPM Download

```
cd /Users/nagag/work/pkgtypes/npm/gallery_server/download
jf npm i iodash --loglevel verbose
npm verb stack HttpErrorGeneral: 403 Forbidden - GET https://psemea.jfrog.io/artifactory/api/npm/nagag-npm-remote/iodash/-/iodash-0.0.1-security.tgz
npm verb stack     at /opt/homebrew/lib/node_modules/npm/node_modules/npm-registry-fetch/lib/check-response.js:95:15
npm verb stack     at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
npm verb statusCode 403
```
