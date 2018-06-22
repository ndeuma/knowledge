# Shell Scripts

* Quickly create a 100 MB file for testing with large files: 
  
  `  dd if=/dev/zero of=100M.dat bs=1kB count=99999`
* Search for a class or package name in \*.jar files: 
  
  `for file in *.jar; do echo "========== ${file} =========="; jar tf $file | grep foo; done`
* Directories that cannot be deleted in Windows Explorer due to too long path names can be deleted in Git Bash using `rm -Rf` 

* Search for files with a given name and copy all found files into some directory, including the folder structure:
  
  `  find . -name '*SE_V6*.jsp' | xargs cp --parents -t /C/Users/Peter/Temp/`
