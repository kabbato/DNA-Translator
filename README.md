# DNA-Translator
Program that takes in a text file containing one or more DNA sequences of any species then translates it to the equivalent sequence for mammals or E.Coli

This program was part of a larger project for a software internship I had at a biotech startup, so a lot of what it includes is based on what the scientists working there requested of me functionality wise

PythonCodonator.py:
Running the program will run a shell script dependent on your OS that should download all the required modules (openpyxl and tkinter, as not all Python installations include tkinter), you should only need to download the file for your OS, which should be named accordingly as "ModuleInstal[OS]". The program will then open a tkinter UI, that has been left mostly unstyled, and from which you can manage all the programs operations. 

PatternTemp.txt:
When entering patterns to translate DNA with, you also have the option to select a text file containing patterns which will then be loaded into the list of patterns and displayed on the UI. A sample file has been provided with some common patterns, but others can be added following the same format. 

inputSequence.txt:
Where you would want to input your DNA sequences. You will stil need to select this file through the UI, but after running a set of input sequences, you can also select another file if you want to run different sets of sequences. The format for sequences should be each sequence on a newline, with no gaps between them. Input can alternately be a sequence of just amino acids, in the format of AFTWG, with each character being the abreviation of a different amino acid. The program will differentiate between DNA and Amino sequences on its own. 

inputsequence_Codonated.xlsx and LargeOutput.txt:
The two primary output files. inputsequence_Codonated will have the typical format of pattern, inputted sequence, amino acid translation, and final DNA translation, with any edits for being unable to match the pattern being highlighted in red on the final translation. For sequences that would go beyond the cell limit of a Microsoft Excel sheet, a separate txt file is used to contain them, and will instead have for reference the number of the input sequence in order from the list of sequences, the pattern used, and the final translation, in a paragraph format.  

mambac.xlsx:
Reference file for DNA translation, has the data that tracks amino acids and their equivalent 3 character DNA pieces by pattern for both mammals and E.Coli, the two subjects of translation provided. More possible species translations can be added if the user adds additional sheets to this Excel file and makes sure to match the format with the existing ones. 
