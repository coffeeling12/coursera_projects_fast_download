From an open Jupyter Notebook homework assignment, select "Coursera" to take you to the home page.
Make a new notebook and fill it with the following and excute the cell with:

    %%bash
    tar cvfz hw.tar.gz .
    
This may take a little while to run depending on the packages.
Select "Coursera" again to take you to the Home directory.
Check the hw.tar.gz file and then Download.
After the file is downloaded, delete it.

If the file is too big, you may get an error and have to restart. If so, try the following instead, remembering to delete any tar files created.

    %%bash
    for dir in */
    do
      base=$(basename "$dir")
      tar -czf "${base}.tar.gz" "$dir"
    done
    
    
