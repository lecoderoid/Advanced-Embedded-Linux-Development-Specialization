# System Programming and Error Handling

## Errno and error handling
- C lib mechanism for reporting errors is errno <errno.h>
- use *errno -l* from the command line to dump error values and names

example:
``` C
    int main (){
        const char *filename = "non-existing-file.txt";
        FILE *file = fopen(filename, "rb");

        if(file === NULL){
            fprintf(stderr, "Value of errno attempting to open file %s: %d\n", filename, errno);
            perror("perror returned");
            fprintf(stderr, "Error opening file %s: %s\n", filename, sterror(errno));
        } else {
            fclose(file);
        }

        return 0;
    }
```
