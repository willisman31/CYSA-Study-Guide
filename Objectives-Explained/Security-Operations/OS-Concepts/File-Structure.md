# File Structure

## Explanation

Not to be confused with the OS's file *system*, file structure refers to a kind of formatting that allows files to be understood by the OS and comes in 3 types:

1. text - characters organized by line
2. object - bytes organized by block
3. source - series of functions/processes

File structures are frameworks for saving data in individual files, file systems are the larger mechanisms used by operating systems to organize files and directories at a higher level.

## Importance

Different file structures communicate different behaviors to the operating system, understanding how these various frameworks can be manipulated can help attack and defend systems more effectively.

## Example

PDF is one of the most common file formats sent between businesses, but it's also very commonly attacked and manipulated.  Between 2014 and 2019, well over 1000 vulnerabilities were reported in the Adobe Acrobat Reader all stemming from its parsing of one type of structure.

## Resources

- [Guru99](https://www.guru99.com/file-systems-operating-system.html)
- [UIC](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/10_FileSystemInterface.html)
- [Infosec Institute - PDF format](https://resources.infosecinstitute.com/topic/pdf-file-format-basic-structure/)
- [MIT Comm Lab](https://mitcommlab.mit.edu/broad/commkit/file-structure/)

# Configuration File Locations

Most global Linux config files will be located in the /etc directory

Windows config files are sprawled much more loosely across the file system; another set of notes explained the Windows registry which holds a lot of configurations; some applications will hold their config files in %APPDATA%; the C:\Windows directory and its subdirectories also hold some configurations.  