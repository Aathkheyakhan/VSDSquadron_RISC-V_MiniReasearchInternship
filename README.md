# VSDSquadron_RISC-V_MiniReasearchInternship
This Github-Repo is to track my progress regarding RISC-V based hands-on project research internship 


# TASK-1

#### Install all the necessary files regarding internship as in riscv_workshop.vdi and visualC++ and oracle virtual-box(which is free and open source virtualization software).Download and do the installation steps and setup virtual machine(its an physical computer but inside a virtual environment)

## STEP:1
#### Open the VDI File using virtual box in windows and open terminal 

## STEP:2
#### Install LEAFPAD (EDITOR)

              sudo apt install LEAFPAD
              
![TASK1 7_29_2024 9_44_26 PM](https://github.com/user-attachments/assets/3a821b2c-156e-4b47-b942-1c5307372a21)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_29_2024 9_45_04 PM](https://github.com/user-attachments/assets/347a1368-63d6-40d1-9b2e-3a4541351fc3)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_29_2024 9_45_37 PM](https://github.com/user-attachments/assets/f28877a1-18e9-4c57-80ec-07a310552c92)


#### run the cd command to make sure we are in home directory 

              cd
              
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_05_09 PM](https://github.com/user-attachments/assets/c9277f82-b3c2-40eb-9f24-be4264fb2edd)


#### To open the file in editor 

             leafpad filename.c &
             
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_06_23 PM](https://github.com/user-attachments/assets/ff033282-a9e4-498d-9b8d-5051dd7d2059)


#### Write a C program to calculate the sum from 1 to n in the leafpad editor 

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_07_26 PM](https://github.com/user-attachments/assets/ee8fea13-cfb2-4efa-85e4-b0cc8e17efd3)


## STEP:3

#### RUN AND COMPLILE THE CODE USING THE FOLLOWING COMMANDS and check the output

             gcc.filename.C
             
             
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_07_41 PM](https://github.com/user-attachments/assets/b875694c-343f-4702-9b99-0325582e2a15)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_09_15 PM](https://github.com/user-attachments/assets/a4189566-4078-4499-91e4-5640724805a2)


             ./a.out
             

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_09_25 PM](https://github.com/user-attachments/assets/6c44adc6-7629-4203-8e22-d4dcf7287b03)
       
## STEP:4

#### COMPILE THE SAME PROGRAM WITH RISC-V SIMULATOR 

            riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o filename.o filename.c
            
            
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_10_49 PM](https://github.com/user-attachments/assets/424deaf2-fef1-48d9-a1c9-e8027c42ac27)

#### To display the CODE IN THE TERMINAL

            cat filename.C
            
            
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_09_41 PM](https://github.com/user-attachments/assets/923de361-3b70-461e-9c10-472065fd88f3)


#### TO generate the file

            ls -ltr filename.o

            
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_11_05 PM](https://github.com/user-attachments/assets/9f080473-bf3f-4333-a673-a8e51ad8408d

## STEP:5

#### ASSEMBLY CODE FOR THE PROGRAM

            riscv64-unknown-elf-objdump -d filename.o 

            
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_12_38 PM](https://github.com/user-attachments/assets/1873f725-b02d-4c6b-bf3b-a6432405f8ea)

#### The above code gives a bunch of assembly code so simplify use the below code.

           riscv64-unknown-elf-objdump -d filename.o | less
           
           
![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_13_07 PM](https://github.com/user-attachments/assets/dd02eb43-376c-42ab-ab2a-22993a16ae8e)



#### (as the above code gives a huge section but we need to Check the values in main and find them out by giving /main and n)


![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_13_25 PM](https://github.com/user-attachments/assets/9c838ea3-8596-42be-acbb-cbeaf746d075)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_13_29 PM](https://github.com/user-attachments/assets/e1a7623a-23b9-4331-a9d2-b576bcbb5c8f)

## STEP:6

#### DISPLAY THE ASSEMBLY CODE 


![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_13_37 PM](https://github.com/user-attachments/assets/ecc4f1a3-2616-4aaf-b1e6-1303d041ba96)

## STEP:7

#### OBSERVE THE SAME BY GIVING Ofast instead of O1 and display the assembly code


![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_14_58 PM](https://github.com/user-attachments/assets/cb1994d7-e498-4491-8d90-569c42d4b662)

#### replace O1 with Ofast in the command

       riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o filename.o filename.c
       

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_14_58 PM](https://github.com/user-attachments/assets/581d3f5f-6b73-47af-8440-48a464d9abbf)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_15_07 PM](https://github.com/user-attachments/assets/da75f5ef-2ac7-48e6-a202-6b39ed211ef9)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_15_11 PM](https://github.com/user-attachments/assets/ba26b1da-e507-48e7-b9f3-b8c251eebc77)

![vsdworkshop  Running  - Oracle VM VirtualBox 7_30_2024 6_16_34 PM](https://github.com/user-attachments/assets/b08eaebb-3797-46b2-923d-d11c59d14d52)

         









