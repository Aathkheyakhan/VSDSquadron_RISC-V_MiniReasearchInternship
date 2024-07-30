# VSDSquadron_RISC-V_MiniReasearchInternship
This Github-Repo is to track my progress regarding RISC-V based hands-on project research internship 


                                                            VSDSquadron_RISC-V_MiniReasearchInternship

TASK-1

Install all the necessary files regarding internship as in riscv_workshop.vdi and visualC++ and oracle virtual-box(which is free and open source virtualization software).Download and do the installation steps and setup virtual machine(its an physical computer but inside a virtual environment)

STEP:1
Open the VDI File using virtual box in windows and open terminal 

STEP:2
Install LEAFPAD (EDITOR)

sudo apt install LEAFPAD

run the cd command to make sure we are in home directory 

cd

To open the file in editor 

leafpad filename.c &

Write a C program to calculate from 1 to n in the leafpad editor 

STEP:3

RUN AND COMPLILING THE CODE USING THE FOLLOWING COMMANDS

gcc.filename.C

./a.out

Check the ouput


STEP:4

COMPILING THE SAME PROGRAM WITH RISC-V SIMULATOR 

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o filename.o filename.c

To display the CODE IN THE TERMINAL

cat filename.C

TO generate the file

ls -ltr filename.o

STEP:5

ASSEMBLY CODE FOR THE PROGRAM

riscv64-unknown-elf-objdump -d filename.o 

The above code gives a bunch of assembly code so simplify use the below code.

riscv64-unknown-elf-objdump -d filename.o | less

(as the above code gives a huge section but we need to Check the values in main and find them out by giving /main and n)

STEP:6

DISPLAY THE ASSEMBLY CODE 

STEP:7

OBSERVE THE SAME BY GIVING Ofast instead of O1

replace O1 with Ofast in the command

riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o filename.o filename.c









