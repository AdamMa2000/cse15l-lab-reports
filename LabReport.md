# Lab Report 1

https://github.com/AdamMa2000/cse15l-lab-reports.git

## Command "cd"

1.

![cd1](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/0de7c38c-6038-4594-ae08-171c500c290c)


When I executed `cd lecture1` I was in the home directory, and when I added the directory name after cd I moved to the Lecture1 directory. This command executes smoothly and I can jump directly to any directory I own.

2.

![cd2](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/b8930568-029f-47bd-ba84-bcb063582493)

When I entered and executed the "cd" command, I was in the [user@sahara ~/lecture1]$ directory. After executing the command, I returned to the home directory from the Lecture1 directory. The meaning of the cd command is Change Directory. We can switch between different paths by adding the path after cd.

3.

![cd3](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/c8beb5bd-cf43-42e8-be79-4585f865a0a6)

When I try to change the directory, the error is displayed because Hello.java is a file name, not a directory, and the cd command changes the working directory, not the file. If you want to view or edit the content, you should use the cat command.

## Command "ls"

1.

![ls1](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/3bc806b3-8fd4-4393-9f7e-6ae1629c21fb)

After using the cd command to enter lecture1, execute the ls command to list all files. I can see the files "Hello.class, Hello.java, messages, README".

2.

![ls2](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/af8c0076-6e78-431e-823a-76ed9fbac701)

After using ls to list the folders in Lecture1, you can continue to use the ls command to enter the messages file. This will list all the file names in the file.

3.

![ls3](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/4e23eed3-4f0c-48e7-b02f-27cc29138617)


After executing the ls command in Lecture1, all the files in the directory are displayed. When I want to use ls to view the contents of Hello.java, only the directory name Hello.java is displayed. This is because there is no directory in the file.

## Command "cat"

1.

![cat1](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/46b74824-af3d-47aa-a112-14adba770d1e)

After executing a file in the Lecture1/messages directory, the contents inside the file will be displayed. I think this is similar to print out.

2.

![cat2](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/cebd6e7b-d030-4ef8-a459-cd7c852f8308)

An error occurred when I tried to cat messages in the lecture1 directory. The reason for this problem is that cat wants to display the text content in the file, not the directory.

3.

![cat3](https://github.com/AdamMa2000/cse15l-lab-reports/assets/86699770/db69496f-a982-41a9-9139-23f39752e7e9)

When I enter cat > wow.txt, a text document named wow will be created. Then command will let me enter the content that the document wants to store. After I enter hello world, I can execute the cat wow.txt file to view it. The content inside is gone.


