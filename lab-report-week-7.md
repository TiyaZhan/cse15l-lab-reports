# Part 1

## Shortest Command used to perform the task `Changing the name of the start parameter and its uses to base`.
```
/start<Enter>cebase<Esc>n.n.:w<Enter>
```
*Total of 21 key pressed*
## Step 1
```
/start<Enter>
```
Below shows the position of cursor before the command. 
![img1](/images/w7-1.1.png)
After the command, the cursor moved to the beginning of the first occurance of `start`. The `/` + `word to search` + `<enter>` command searches for the `word to search` in the file.
![img2](/images/w7-1.2.png)

## STEP 2
```
ce
```
The image below shows the result of typing command `ce`. `ce` switches to insert mode and means to change until the end of the word. In this case, it deletes the word `start`.
![img3](/images/w7-2.1.png)
## STEP 3
```
base<Esc>
```
The image below shows the result of typing in `base`. Since we are in insert mode typing in the word `base` replaces `start` to `base`. 
![img4](/images/w7-3.1.png)
The image below shows the result of pressing `<Esc>`. The key `<Esc>` menas to exit the insert mode and back to normal mode, so you can see we are no longer in insert mode. 

![img5](/images/w7.3.2.png)
## STEP 4
```
n.
```
The key `n` finds the next matches of the word `start` based on the search command `/start`. It moves the cursor to the beginning of the next occurence of `start` shown in the below image.
![img6](/images/w7-5.1.png)
The key `.` means to repeat the last command, so it repeats `cebase<Esc>` commands which deletes `start` and replace it with `base`. The result after the `.` command is shown below. 
![img7](/images/w7-5.2.png)
## STEP 5
```
n.
```
The same command is used as step 4. First, `n` is pressed, which finds the next occurance of `start` and moves the cursor to that position. The moved cursor is shown in the below image.
![img8](/images/w7-6.1.png)
Then, `.` is pressed which repeats the `cebase<Esc>` command. `start` is deleted and replaced with `base`. The result after `.` command is shown below. 
![img9](/images/w7-6.2.png)
## STEP 6
```
:w<Enter>
```
Since there are only three `start` inside the getFile() method, we can now save the changes to the file. `:w<Enter>` is used to save the file. The image below shows the typing of `:w` command.
![img10](/images/w7-7.1.png)
The image below shows the result after pressing `<Enter>`.
![img11](/images/w7-7.2.png)

# PART 2

For the strategy to edit locally using vs code and `scp` to the remote computer, I used about 40 seconds. One difficuties that I encountered is that when I log in to the remote computer, I always forgot to change the directory to the one that contains the files. This step wasted some time. 

For the strategy to edit the file remotely using vim, I used around 38 seconds. One difficulties that I encountered is that I always forgt the command that I need to type inside of vim, so I have to stop and repeat the process several time to get the best time. Even the shortest command that I came up with still have 21 keys, so it is hard to remember all of them and know which one to press next spontaneously.

- Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?

I would prefer to use the scp way to do it if I have access to the file locally. I'm more use to using vs code then vim. Also, IDE like vs code checks for errors as you program. It provides useful warning and suggestions. In vim, it won't even tell you if you are missing one side of the bracket, {}.
- What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)

If I don't have acess to the file locally, I will use vim to edit the file on the remote computer. Also, if the changes that I need to make is very minor, like a few line changes, I would consider using vim. It might be more efficient to directly edit the file remotely if we are just modifying a few lines. Like, changing the variables naming might be easier to do it using vim than locally. You can direcly test it out remotely right after the changes are made. 