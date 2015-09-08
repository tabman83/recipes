remove-node-modules-folder
==========================
While trying to remove the node_modules folder from npm you get the following error message:
> The source file name(s) are larger than is supported by the file system. Try moving to a location which has a shorter path name, or try renaming to shorter name(s) before attempting this operation.
Then you are unable to remove such folder. This applies to windows only.

Following is the procedure to successfully remove the folder.

Install rimraf globally:
```
npm install rimraf -g
```

Once done, issue the following:
```
rimraf node_modules
```
