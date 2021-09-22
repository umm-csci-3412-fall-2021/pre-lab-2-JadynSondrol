# Leak Report

Once the isclean method compares the original string to the cleaned version the memory allocated to cleaned is never used again and is never deallocated which caused the memory leak. 

To fix this I checked if cleaned was empty and if it wasn't I freed the memory that was allocated to it.
