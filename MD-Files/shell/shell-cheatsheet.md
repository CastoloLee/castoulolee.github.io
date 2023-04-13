# Cheatsheet - Shell

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky"><strong>Command</strong></th>
    <th class="tg-0pky"><strong>Description</strong></th>
    <th class="tg-0pky"><strong>Syntax</strong></th>
    <th class="tg-0pky"><strong>Example</strong></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">alias</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">alias &lt;alias_name&gt;='&lt;command_to_execute&gt;'</td>
    <td class="tg-0pky">alias pd='pwd'</td>
  </tr>
  <tr>
    <td class="tg-0pky">touch</td>
    <td class="tg-0pky">Creates a new file without content, changes the timestamp for existing files</td>
    <td class="tg-0pky">touch &lt;filename&gt;</td>
    <td class="tg-0pky">touch test.txt</td>
  </tr>
  <tr>
    <td class="tg-0pky">rm / rmdir</td>
    <td class="tg-0pky">is used for deleting files and directories</td>
    <td class="tg-0pky">rm &lt;filename&gt;</td>
    <td class="tg-0pky">rm test.txt</td>
  </tr>
  <tr>
    <td class="tg-0pky">man</td>
    <td class="tg-0pky">provides help for the given command (also called manual page)</td>
    <td class="tg-0pky">man &lt;command_name&gt;</td>
    <td class="tg-0pky">man ls</td>
  </tr>
  <tr>
    <td class="tg-0pky">mkdir</td>
    <td class="tg-0pky">is used to create a new directory</td>
    <td class="tg-0pky">mkdir &lt;directory_name&gt;</td>
    <td class="tg-0pky">mkdir my_directory</td>
  </tr>
  <tr>
    <td class="tg-0pky">help</td>
    <td class="tg-0pky">Provides assistance with commands, displays possible options.</td>
    <td class="tg-0pky">help &lt;command_name&gt;</td>
    <td class="tg-0pky">help cd</td>
  </tr>
  <tr>
    <td class="tg-0pky">cd</td>
    <td class="tg-0pky">is used to change to another directory</td>
    <td class="tg-0pky">cd &lt;directory_name&gt;</td>
    <td class="tg-0pky">cd my_directory</td>
  </tr>
  <tr>
    <td class="tg-0pky">echo</td>
    <td class="tg-0pky">is used to output arbitrary content to the shell, is an alternative to printf may</td>
    <td class="tg-0pky">echo &lt;string_value&gt;</td>
    <td class="tg-0pky">echo "Hello World"</td>
  </tr>
  <tr>
    <td class="tg-0pky">cp</td>
    <td class="tg-0pky">is used to create a copy of a file or directory</td>
    <td class="tg-0pky">cp &lt;source_file&gt; &lt;destination_file&gt;</td>
    <td class="tg-0pky">cp test.txt my_directory/test.txt</td>
  </tr>
  <tr>
    <td class="tg-0pky">fdisk</td>
    <td class="tg-0pky">fdisk is a command that allows you to manage partitions on a hard disk. It can be used to create, delete, modify and move partitions and change their types. It can also display information about existing partitions.</td>
    <td class="tg-0pky">fdisk &lt;disk_name&gt;</td>
    <td class="tg-0pky">fdisk /dev/sda</td>
  </tr>
  <tr>
    <td class="tg-0pky">mv</td>
    <td class="tg-0pky">allows to move files and/or directories to another place in the file system </td>
    <td class="tg-0pky">mv &lt;source_file&gt; &lt;destination_file&gt;</td>
    <td class="tg-0pky">mv test.txt my_directory/test.txt</td>
  </tr>
  <tr>
    <td class="tg-0pky">ls</td>
    <td class="tg-0pky">prints a list with all files, links and directories contained in a directory</td>
    <td class="tg-0pky">ls [-l]</td>
    <td class="tg-0pky">ls -l</td>
  </tr>
</tbody>
</table>

## Automation with Scripts

Automating certain tasks on a computer system has obvious advantages: tasks are no longer forgotten, and recurring activities no longer need to be done manually. At the beginning of any process automation in the data center, the implementation of a corresponding solution is necessary.

##### Reasons for Automation
Today's IT infrastructures are more complex than ever. They include more applications, more physical and virtual servers, larger global networks, and more data, all of which require significant administrative effort. For businesses, it is not cost-effective to solve this problem by continually increasing the number of employees. Rather, they must look for solutions to manage this growth efficiently. Furthermore, many companies struggle to retain the knowledge they have within their organization. Automating IT processes can help automate the processing of alerts and incidents, improve infrastructure uptime, and reduce operating costs.

##### Operating system command-line interpreters
Some programming languages are derived from the command-line interpreters of operating systems. The interpreters are primarily designed for interactive use, i.e., for entering commands. The input language is extended with variables, arithmetic expressions, control structures, and other elements that enable the automation of tasks (e.g., during unattended installation) by writing small programs in files. These files can then be executed by the interpreter. In the field of scripting languages, there is a variety of languages. We are interested in script languages derived from the command-line interpreters of operating systems:
- Windows PowerShell - command interpreter for Microsoft Windows
- bash - GNU replacement and extension of the Unix Bourne shell
- cmd.exe - command interpreter of newer Windows versions from Windows NT onwards
Under the Unix/Linux operating system, these files are called shell scripts (executed by one of the Unix shells sh, csh, etc.), while under DOS and Windows, they are also called batch scripts (executed by command.com and cmd.exe).

##### Basics of structured programming
Structured programming is a programming development method that assumes a program structure with uniform and independent program components and describes the conditions under which they interact. The goal of structured programming is to represent algorithms in a way that their sequence is easy to understand and modify. The method was developed by Nassi-Shneiderman and has been one of the strongest impetuses for productive programming development since the 1960s. As in all of IT, the basic principle of IT applies here, namely the so-called EVA principle:
- Input
- Processing
- Output
To solve a task as a system administrator, I need to know what the program should deliver, i.e., what should be output at the end (in whatever form). Next, I have to think about which formulas I need or which parameters are needed. After that, it becomes clear what needs to be entered (and that is not always done via the keyboard).

Computer applications can generally be reduced to a common denominator: they process information.

##### Basic program structures
When algorithms are translated into a machine-readable form, the following three basic program structures always appear, regardless of the programming language:
- Instructions
- Branches based on conditions
- Loops with repetitions
These program structures are implemented in the program code according to the available elements (keywords) of the programming language. These basic program structures are sufficient to describe (almost) all algorithms.

###### The Sequence (Instruction)
A processor is largely occupied with processing command after command of a program in sequence; we speak of a sequential process. In every programming language, the sequence (instruction) is a fundamental program structure.

###### Selection (Choice)
Program branching based on certain conditions is part of the basic instruction set of all processors. At branch points, two or more alternatives can continue.

###### Iteration (Loop)
With iterations (loops), a program can repeat a set of instructions multiple times. The number of repetitions can be determined

##### Tools for processing information

To develop computer applications that can process information, appropriate tools are needed. Programming languages provide these tools.

##### Storing information in variables

A variable is a pointer to a memory location in the computer. Computers process only one instruction at a time; with the help of variables, we can store information at one step in the program and use it again at a later time. Each variable has a specific type that must be explicitly defined before use.

##### Linking and processing information with operators

However, a program is not created solely by storing information. After all, your application should process information, such as performing a calculation and adding two numbers, for example. You can store numbers with variables, but how are they added together? Information processing operations, such as adding numbers, are possible with operators. Every programming language offers operators - without operators, information cannot be processed. Most programming languages have similar operators, each with the same meaning.

##### Controlling the flow with control structures

With the help of variables and operators, you can now process information, such as numbers. However, this processing is only linear so far. The computer processes your instructions in the program from top to bottom, one instruction at a time. But if you want to develop a password protection, for example, access to the secured resource must be granted or not, depending on the user's input. Branching the program flow is possible with control structures.

##### Recurring code sections in functions

Functions are used to enter frequently recurring code sections (calculations, shapes, etc.) only once, and then be able to call them repeatedly. Typically, functions return something (the result of the calculation).

##### Representing processes with flowcharts

A program flowchart (PFC) is a flowchart or program structure plan that is a graphical representation of an algorithm in a program and describes the sequence of operations for solving a task. The symbols for program flowcharts are standardized in DIN 66001. Program flowcharts are often used to represent processes and activities independently of computer programs (e.g., as a description of the workflow for creating a quote in a trading company).

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax"><strong>Command</strong></th>
    <th class="tg-0lax"><strong>Syntax</strong></th>
    <th class="tg-0lax"><strong>Description</strong></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">chmod +x dev.sh</td>
    <td class="tg-0lax">chmod +x FILENAME</td>
    <td class="tg-0lax">lets you execute the shell script</td>
  </tr>
  <tr>
    <td class="tg-0lax">bash -v dev.sh</td>
    <td class="tg-0lax">bash -v FILENAME</td>
    <td class="tg-0lax">prints shell inputs lines as they are read</td>
  </tr>
  <tr>
    <td class="tg-0lax">bash -x dev.sh</td>
    <td class="tg-0lax">bash -x FILENAME</td>
    <td class="tg-0lax">prints the commands and their arguments as they are executed</td>
  </tr>
  <tr>
    <td class="tg-0lax">bash --debugger dev.sh</td>
    <td class="tg-0lax">bash --debugger FILENAME</td>
    <td class="tg-0lax">Arrange for the debugger profile&nbsp;&nbsp;&nbsp;to be executed before the shell starts. &nbsp;&nbsp;&nbsp;Turns on extended debugging mode (see the description of the extdebug&nbsp;&nbsp;&nbsp;option to the shopt builtin below).</td>
  </tr>
</tbody>
</table>
