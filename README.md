# DNA-Translator
Program that takes in a text file containing one or more DNA sequences of any species then translates it to the equivalent sequence for mammals or E.Coli. 

This program was part of a larger project for an internship I had at a biotech startup, so a lot of what it includes is based on what the scientists working there requested of me functionality wise. This was something I developed from scratch, independently, over the course of 2-3 months during my internship. Unfortunately, the version here is only the final version, as I wasn't actively keeping track of the versions I went through over those 2-3 months. 

Right now the program works mostly using txt files and Excel sheets for input and output with a basic Tkinter UI to navigate through the program, but if I have the chance to work on it more, I'd like to improve the UI and also see if there's a better way to handle some of the input and output that doesn't involve dealing with so many other files. Overall, the program was a very good learning experience for me on using Excel files with Python and building a UI with Tkinter, as well as developing a program to meet work/professional expectations. 

# PythonCodonator.py:
Running the program will run a shell script dependent on your OS that should download all the required modules (openpyxl and tkinter, as not all Python installations include tkinter), you should only need to download the file for your OS, which should be named accordingly as "ModuleInstal[OS]". It is also important to keep all of the files in the same directory. 

# PatternTemp.txt:
When entering patterns to translate DNA with, you also have the option to select a text file containing patterns which will then be loaded into the list of patterns and displayed on the UI. A sample file has been provided with some common patterns, but others can be added following the same format. 

# inputSequence.txt:
Where you would want to input your DNA sequences. You will stil need to select this file through the UI, but after running a set of input sequences, you can also select another file if you want to run different sets of sequences. The format for sequences should be each sequence on a newline, with no gaps between them. Input can alternately be a sequence of just amino acids, in the format of AFTWG, with each character being the abreviation of a different amino acid. The program will differentiate between DNA and Amino sequences on its own. 

# inputsequence_Codonated.xlsx and LargeOutput.txt:
The two primary output files. inputsequence_Codonated will have the typical format of pattern, inputted sequence, amino acid translation, and final DNA translation, with any edits for being unable to match the pattern being highlighted in red on the final translation. For sequences that would go beyond the cell limit of a Microsoft Excel sheet, a separate txt file is used to contain them, and will instead have for reference the number of the input sequence in order from the list of sequences, the pattern used, and the final translation, in a paragraph format.  

# mambac.xlsx:
Reference file for DNA translation, has the data that tracks amino acids and their equivalent 3 character DNA pieces by pattern for both mammals and E.Coli, the two subjects of translation provided. More possible species translations can be added if the user adds additional sheets to this Excel file and makes sure to match the format with the existing ones. 
