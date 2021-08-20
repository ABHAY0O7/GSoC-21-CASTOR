##>These are the result of depclean analysis on a demo project without the multi-module analysis feature.

``` java

[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO] 
[INFO] abhayPlugin                                                        [pom]
[INFO] abhay-module-1                                                     [jar]
[INFO] abhay-module-2                                                     [jar]
[INFO] abhay-module-3                                                     [jar]
[INFO] 
[INFO] -----------------------< org.abhay:abhayPlugin >------------------------
[INFO] Building abhayPlugin 1.0-SNAPSHOT                                  [1/4]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhayPlugin ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[INFO] Skipping because packaging type pom.
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-1 >----------------------
[INFO] Building abhay-module-1 1.0-SNAPSHOT                               [2/4]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-1 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [0]: 
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [0]: 
POTENTIALLY UNUSED DIRECT DEPENDENCIES [0]: 
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [0]: 
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-2 >----------------------
[INFO] Building abhay-module-2 1.0-SNAPSHOT                               [3/4]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-2 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [1]: 
	com.fasterxml.jackson.core:jackson-core:2.12.2:compile (size unknown)
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [0]: 
POTENTIALLY UNUSED DIRECT DEPENDENCIES [3]: 
	commons-codec:commons-codec:1.15:compile (size unknown)
	com.jcabi:jcabi-manifests:1.1:compile (size unknown)
	commons-io:commons-io:2.8.0:compile (size unknown)
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [2]: 
	org.slf4j:slf4j-api:1.7.5:compile (size unknown)
	com.jcabi:jcabi-log:0.14:compile (size unknown)
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-3 >----------------------
[INFO] Building abhay-module-3 1.0-SNAPSHOT                               [4/4]
[INFO] --------------------------------[ jar ]---------------------------------
[WARNING] Could not transfer metadata org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from/to example-repo (C:\Users\ABHAY SINGH/.m2/repository): Cannot access C:\Users\ABHAY SINGH/.m2/repository with type default using the available connector factories: BasicRepositoryConnectorFactory
[WARNING] Failure to transfer org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from C:\Users\ABHAY SINGH/.m2/repository was cached in the local repository, resolution will not be reattempted until the update interval of example-repo has elapsed or updates are forced. Original error: Could not transfer metadata org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from/to example-repo (C:\Users\ABHAY SINGH/.m2/repository): Cannot access C:\Users\ABHAY SINGH/.m2/repository with type default using the available connector factories: BasicRepositoryConnectorFactory
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-3 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [1]: 
	org.abhay:abhay-module-2:1.0-SNAPSHOT:compile (size unknown)
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [3]: 
	commons-codec:commons-codec:1.15:compile (size unknown)
	com.fasterxml.jackson.core:jackson-core:2.12.2:compile (size unknown)
	com.jcabi:jcabi-manifests:1.1:compile (size unknown)
POTENTIALLY UNUSED DIRECT DEPENDENCIES [0]: 
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [3]: 
	org.slf4j:slf4j-api:1.7.5:compile (size unknown)
	com.jcabi:jcabi-log:0.14:compile (size unknown)
	commons-io:commons-io:2.8.0:compile (size unknown)
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for abhayPlugin 1.0-SNAPSHOT:
[INFO] 
[INFO] abhayPlugin ........................................ SUCCESS [  0.878 s]
[INFO] abhay-module-1 ..................................... SUCCESS [  1.306 s]
[INFO] abhay-module-2 ..................................... SUCCESS [  1.285 s]
[INFO] abhay-module-3 ..................................... SUCCESS [  1.249 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  4.841 s
[INFO] Finished at: 2021-08-12T17:17:08+05:30
[INFO] ------------------------------------------------------------------------

```

## And now, these are the result of depclean (new) analysis on a demo project with the multi-module analysis feature.

``` java

[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO] 
[INFO] abhayPlugin                                                        [pom]
[INFO] abhay-module-1                                                     [jar]
[INFO] abhay-module-2                                                     [jar]
[INFO] abhay-module-3                                                     [jar]
[INFO] 
[INFO] -----------------------< org.abhay:abhayPlugin >------------------------
[INFO] Building abhayPlugin 1.0-SNAPSHOT                                  [1/4]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhayPlugin ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[INFO] Skipping because packaging type pom.
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-1 >----------------------
[INFO] Building abhay-module-1 1.0-SNAPSHOT                               [2/4]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-1 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [0]: 
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [0]: 
POTENTIALLY UNUSED DIRECT DEPENDENCIES [0]: 
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [0]: 
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-2 >----------------------
[INFO] Building abhay-module-2 1.0-SNAPSHOT                               [3/4]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-2 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [1]: 
	com.fasterxml.jackson.core:jackson-core:2.12.2:compile (size unknown)
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [0]: 
POTENTIALLY UNUSED DIRECT DEPENDENCIES [3]: 
	commons-codec:commons-codec:1.15:compile (size unknown)
	com.jcabi:jcabi-manifests:1.1:compile (size unknown)
	commons-io:commons-io:2.8.0:compile (size unknown)
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [2]: 
	org.slf4j:slf4j-api:1.7.5:compile (size unknown)
	com.jcabi:jcabi-log:0.14:compile (size unknown)
[INFO] 
[INFO] ----------------------< org.abhay:abhay-module-3 >----------------------
[INFO] Building abhay-module-3 1.0-SNAPSHOT                               [4/4]
[INFO] --------------------------------[ jar ]---------------------------------
[WARNING] Could not transfer metadata org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from/to example-repo (C:\Users\ABHAY SINGH/.m2/repository): Cannot access C:\Users\ABHAY SINGH/.m2/repository with type default using the available connector factories: BasicRepositoryConnectorFactory
[WARNING] Failure to transfer org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from C:\Users\ABHAY SINGH/.m2/repository was cached in the local repository, resolution will not be reattempted until the update interval of example-repo has elapsed or updates are forced. Original error: Could not transfer metadata org.abhay:abhay-module-2:1.0-SNAPSHOT/maven-metadata.xml from/to example-repo (C:\Users\ABHAY SINGH/.m2/repository): Cannot access C:\Users\ABHAY SINGH/.m2/repository with type default using the available connector factories: BasicRepositoryConnectorFactory
[INFO] 
[INFO] --- depclean-maven-plugin:2.0.2-SNAPSHOT:depclean (default-cli) @ abhay-module-3 ---
-------------------------------------------------------
[INFO] Starting DepClean dependency analysis
[WARNING] Dependencies were not copied locally
-------------------------------------------------------
 D E P C L E A N   A N A L Y S I S   R E S U L T S
-------------------------------------------------------
USED DIRECT DEPENDENCIES [1]: 
	org.abhay:abhay-module-2:1.0-SNAPSHOT:compile (size unknown)
USED INHERITED DEPENDENCIES [0]: 
USED TRANSITIVE DEPENDENCIES [3]: 
	commons-codec:commons-codec:1.15:compile (size unknown)
	com.fasterxml.jackson.core:jackson-core:2.12.2:compile (size unknown)
	com.jcabi:jcabi-manifests:1.1:compile (size unknown)
POTENTIALLY UNUSED DIRECT DEPENDENCIES [0]: 
POTENTIALLY UNUSED INHERITED DEPENDENCIES [0]: 
POTENTIALLY UNUSED TRANSITIVE DEPENDENCIES [3]: 
	org.slf4j:slf4j-api:1.7.5:compile (size unknown)
	com.jcabi:jcabi-log:0.14:compile (size unknown)
	commons-io:commons-io:2.8.0:compile (size unknown)

-------------------------------------------------------
[INFO] DEPENDENT MODULES FOUND
Due to dependent modules, the debloated result of some dependencies from previous modules has been changed now.
The dependency-module details of such dependencies with the new results are as follows :

	1) ModuleCoordinates : org.abhay:abhay-module-2:1.0-SNAPSHOT
	   DependencyCoordinates : com.jcabi:jcabi-manifests:1.1:compile
	   OldType : unusedDirect
	   NewType : usedDirect

	2) ModuleCoordinates : org.abhay:abhay-module-2:1.0-SNAPSHOT
	   DependencyCoordinates : commons-codec:commons-codec:1.15:compile
	   OldType : unusedDirect
	   NewType : usedDirect

-------------------------------------------------------
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for abhayPlugin 1.0-SNAPSHOT:
[INFO] 
[INFO] abhayPlugin ........................................ SUCCESS [  0.878 s]
[INFO] abhay-module-1 ..................................... SUCCESS [  1.306 s]
[INFO] abhay-module-2 ..................................... SUCCESS [  1.285 s]
[INFO] abhay-module-3 ..................................... SUCCESS [  1.249 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  4.841 s
[INFO] Finished at: 2021-08-12T17:17:08+05:30
[INFO] ------------------------------------------------------------------------
```

### PS: If anyone wants see the demo project then he/she may [visit here](https://github.com/ABHAY0O7/multi-module-project)