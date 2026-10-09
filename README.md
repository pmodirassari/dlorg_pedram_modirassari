# dlorg_pedram_modirassari
linux_lab-1 - dbda26

Task 0 - warm-up:
  1. Created repo, connected to vm through SSH, created dlorg bash file with a shebang for future bash script and pushed to git repo
  2. created .gitignore file by copying & pasting, gave permissions to be able to execute the dlorg file by chmod +x, then pushed to git again
  3. started writing this description of my procedure

Task 1-2 - the Download Organizer
  1. I created random files by touch text{1..4}.txt camera{1..4].raw paint{1..3}.jpg film{1..4}.avi video{1..2}.wmv song{a,b,c,d}.mp3 soundclip{1..4}.wav scanned{1..4}.pdf present{1..3}.pptx
  d<img width="653" height="187" alt="Screenshot 2026-10-06 123204" src="https://github.com/user-attachments/assets/bd555e75-8e03-4136-9d85-582d3f2e7dc6" />
  2. Wrote script after reviewing bash conditionals and bash loops. Went for case first but changed it to if later. Hade some problems getting the different files on the same row because I used | as a seperator, but I then found with the help if LLM that in the case of case its one | and in the case of if it's two ||'s.
  3. I run the script and after correcting a few typos I got it to work
     <img width="1285" height="945" alt="Screenshot 2026-10-07 132204" src="https://github.com/user-attachments/assets/df0445f0-b160-4d13-8806-5c0934f81228" />

Task 3-4
  1. I placed a link to my script in .local/bin, then created a service and a unit-file with dlorg.service in .config/systemd so that the script will get started after every re-boot. I followed the instructions from class (with "sudo systemctl daemon-reload, enabling and starting) but I had to come up with a way for it not to only be "oneshot", but be running continuously. So I asked LLM for the command to substitute "oneshot", and it gave me the suggestion of making a dlorg.path file with similar structure as the dlorg.service. I hence went through the same procedure with this file > dameon-reload > enable > start). And now I think everything works as it should. I have tested creating and moving in files of different types into the Downloads-folder and they all get placed automatically where they should.
<img width="525" height="998" alt="Screenshot 2026-10-07 153049" src="https://github.com/user-attachments/assets/71f8aa4b-895e-4487-8a75-8840aca70f3f" />

<img width="723" height="950" alt="Screenshot 2026-10-08 105344" src="https://github.com/user-attachments/assets/b287cfe7-4439-432c-bfbc-5ba06913cf87" />

<img width="670" height="667" alt="Screenshot 2026-10-08 110611" src="https://github.com/user-attachments/assets/1333ab34-98c3-4f53-ab4e-5613df8e3a8d" />

<img width="681" height="668" alt="Screenshot 2026-10-08 111130" src="https://github.com/user-attachments/assets/bf1d9ef1-e8df-4780-b713-4a930df90bc6" />

