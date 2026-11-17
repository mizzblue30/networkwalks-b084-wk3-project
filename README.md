# networkwalks-b084-wk3-project
Password Cracking with John the Ripper (JTR), Johnny & Networkwalks Tool

Cybersecurity & Ethical Hacking — Week 3 Practical Project

Author: Sakinah Abubakar
Programme: Networkwalks Internship Program
Project: Password Cracking and Capture The Flag (CTF) Exercises

---

1. Introduction

Password cracking is an important aspect of cybersecurity, particularly in penetration testing, security auditing and vulnerability assessment. It involves attempting to recover passwords from password hashes or encrypted files using techniques such as dictionary attacks, brute-force attacks and rule-based password guessing.

As part of my practical training under the Networkwalks Internship Program, I completed two structured practical modules focused on password recovery and Capture The Flag (CTF) challenges.

In Module 1, I explored offline PDF password cracking using John the Ripper (JTR), its Command-Line Interface (CLI), and Johnny, its Graphical User Interface (GUI). I extracted password hashes from three encrypted PDF documents, prepared the hashes for processing and successfully recovered all three passwords.

In Module 2, I used the Networkwalks password-cracking tool to analyse and crack three additional encrypted PDF documents. I successfully recovered the passwords and verified access to all three documents.

Across both modules, I worked with six encrypted PDF files, successfully recovered all six passwords and captured three distinct Networkwalks CTF flags.

2. Objectives

The objectives of these practical exercises were to:

- Understand the fundamentals of password cracking and hash extraction.
- Install and configure John the Ripper on a Windows environment.
- Understand the relationship between John the Ripper and Johnny.
- Extract password hashes from encrypted PDF documents.
- Perform dictionary-based password attacks using CLI and GUI environments.
- Explore the functionality of the Networkwalks password-cracking tool.
- Recover passwords from multiple encrypted PDF documents.
- Verify recovered passwords by unlocking the original documents.
- Capture and document the required CTF flags.

3. Tools and Technologies Used

Tool| Purpose
John the Ripper (JTR)| Core password-cracking engine used for offline password recovery.
Johnny| Graphical front-end for managing John the Ripper cracking sessions.
Networkwalks Cracking Tool| Web-based tool used for the second practical exercise.
OnlineHashCrack PDF Hash Extractor| Used to extract password hashes from encrypted PDF documents.
Notepad| Used to save extracted hashes as text files.
Windows PC| Host operating environment for the practical exercises.

4. Module 1: Offline PDF Password Cracking Using John the Ripper and Johnny

4.1 Practical Overview

The first practical module focused on offline password recovery using John the Ripper and Johnny.

I worked with three encrypted PDF documents:

1. My Locked PDF1.pdf
2. My Locked PDF2.pdf
3. My Locked PDF3.pdf

Each document required an individual hash extraction process. The extracted hashes were saved separately as text files before being loaded into the cracking environment.

I explored both command-line and graphical approaches to understand how password-cracking operations can be performed using different interfaces.

4.2 Installation and Configuration

I downloaded John the Ripper for Windows from the official Openwall website.

After downloading the package, I extracted its contents to access the executable files required to run the password-cracking engine.

I also downloaded and installed Johnny (version 2.2), the graphical interface designed to interact with John the Ripper.

After installation, I launched Johnny and navigated to:

Settings → Browse

I located the "john.exe" executable inside the extracted John the Ripper directory and selected it.

This configured Johnny to use the John the Ripper engine for password-cracking operations.

4.3 PDF Hash Extraction

To prepare the encrypted PDF documents for password cracking, I used the OnlineHashCrack PDF Hash Extractor.

Each of the three PDF documents was processed individually, generating a corresponding password hash in the "$pdf$" format.

The extracted hashes were copied and saved using Notepad with the following filenames:

Target PDF| Extracted Hash File
My Locked PDF1.pdf| hash1.txt
My Locked PDF2.pdf| hash2.txt
My Locked PDF3.pdf| hash3.txt

During preparation, I ensured that each hash was correctly formatted. Unwanted characters, such as leading byte-string notation or additional quotation marks, were removed to prevent formatting issues when loading the files into John the Ripper.

4.4 Loading Hashes and Executing the Attack

After preparing the hash files, I launched Johnny and selected the Open password file option.

I loaded the corresponding hash text files and selected the PDF format.

I then initiated the cracking process by selecting Start new attack.

John the Ripper executed its password-cracking process against the supplied hashes, testing password candidates until matching passwords were identified.

This process was repeated for all three encrypted PDF documents.

4.5 Password Recovery Results

All three encrypted PDF documents were successfully cracked using John the Ripper through the CLI/GUI workflow.

The recovered passwords were:

Target File| Hash File| Recovered Password| Status
My Locked PDF1.pdf| hash1.txt| "good luck"| Successfully Cracked
My Locked PDF2.pdf| hash2.txt| "password1"| Successfully Cracked
My Locked PDF3.pdf| hash3.txt| "1qAZ2WSX"| Successfully Cracked

4.6 Password Verification

Following password recovery, I opened each original encrypted PDF document and entered its corresponding recovered password.

All three documents unlocked successfully, confirming that the recovered passwords were correct.

This completed the first practical module.

---

5. Module 2: Password Cracking Using the Networkwalks Tool

5.1 Practical Overview

The second practical module involved using the dedicated Networkwalks password-cracking tool to evaluate three additional encrypted PDF documents.

Unlike the previous exercise, which focused on John the Ripper and Johnny, this module provided an opportunity to work with the platform's integrated cracking tool and assess its performance against multiple PDF targets.

The three target documents were tested individually to recover their passwords.

5.2 Target File Analysis and Results

All three PDF documents were successfully processed using the Networkwalks password-cracking tool.

The results were as follows:

Target File| Recovered Password| Status
My Locked PDF 1| "password1"| Successfully Cracked
My Locked PDF 2| "password1"| Successfully Cracked
My Locked PDF 3| "1qaz2wsx"| Successfully Cracked

5.3 Extracted PDF Hash

The Networkwalks tool generated PDF-specific hash information in the "$pdf$" format.

An example of the extracted hash structure is shown below:

$pdf$4*4*128*-1028*1*16*34eb542eff4e1b0b32d25ce15a9a7281*32*b77872bfc9a24fb2f845066283a8fc1b0021446990b9e4114071a4d9104984c1*32*e7572256e4b552cd57988f5134214b91920d94d7a6bf********************

The extracted hash represents the password information used during the cracking process.

5.4 Password Recovery and Verification

After the cracking process, I obtained the recovered passwords for the three target PDF documents.

I subsequently used the recovered credentials to access the corresponding protected documents.

All three PDFs were successfully unlocked, confirming the validity of the recovered passwords.

This completed the second practical module.

---

6. Capture The Flag (CTF) Results

As part of the practical exercises, I completed the required verification challenges and captured three distinct Networkwalks CTF flags.

The flags served as confirmation of successful completion of the associated practical tasks.

Challenge| Captured Flag
Challenge 1: Initial File Cracking| "nw{cybersecurity_flag_captured_2608}"
Challenge 2: John the Ripper Persistence| "nw{networkwalks_persistence_jtr_270521}"
Challenge 3: Final Lab Completion| "nw{networkwalks_flag_260821_1}"

These flags were captured and documented as evidence of my practical achievements across the exercises.

---

7. Technical Findings and Security Analysis

The two practical modules provided hands-on experience with different approaches to password cracking and offline password recovery.

One significant finding was that all six encrypted PDF documents were successfully cracked across the two modules.

The exercises demonstrated the importance of extracting password hashes correctly before attempting password recovery. They also highlighted how dictionary-based attacks can identify weak or predictable passwords.

For example, passwords such as "password1" and "1qAZ2WSX" demonstrate how familiar words, predictable numerical combinations and common keyboard patterns can create password weaknesses.

The exercises also reinforced the distinction between hash extraction and password cracking. Extracting a hash prepares the password information for analysis, while the cracking tool attempts to identify a candidate that matches the extracted hash.

Security Recommendations

Based on the findings of these exercises, the following security practices are recommended:

1. Use long, unique and unpredictable passwords.
2. Avoid common dictionary words and predictable numerical suffixes.
3. Avoid easily identifiable keyboard patterns.
4. Use password managers to generate and securely store strong passwords.
5. Apply appropriate encryption and password protection to sensitive documents.
6. Conduct periodic password-strength assessments to identify weak credentials.

---

8. Challenges Encountered and Observations

The main challenge encountered during the practical exercises was extracting the downloaded John the Ripper package and preparing it for use in the Windows environment.

After successfully extracting the package, I proceeded with the configuration of Johnny and the remaining password-cracking activities without significant difficulties.

The subsequent tasks were completed successfully, and all six encrypted PDF documents were cracked and unlocked.

An important observation from the exercises was how different interfaces and tools can be used to perform password-cracking operations. John the Ripper provided the underlying cracking engine, Johnny offered a graphical interface for managing the process, while the Networkwalks tool provided another environment for practical password recovery.

Overall, the exercises reinforced my understanding of password-cracking workflows and the importance of proper tool configuration and hash preparation.

---

9. Conclusion

Completing these two practical modules provided valuable hands-on experience with password-cracking tools and offline password recovery techniques.

In Module 1, I successfully used John the Ripper and Johnny to extract, process and crack the password hashes of three encrypted PDF documents.

In Module 2, I used the Networkwalks password-cracking tool to recover the passwords of three additional encrypted PDF documents.

Across both modules, all six target PDFs were successfully cracked and unlocked. I also captured three Networkwalks CTF flags as verification of my practical achievements.

The exercises strengthened my understanding of PDF hash extraction, dictionary-based attacks, CLI and GUI password-cracking environments, password recovery and CTF verification.

Beyond completing the exercises, I gained practical familiarity with tools used in password security assessments and developed a better understanding of how weak passwords can expose protected information.

---

10. Visual Evidence

The screenshots below provide visual documentation of the practical exercises, tools used, password recovery processes and CTF results obtained across both modules.
<<img width="1920" height="1080" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/9963ea20-1685-4b40-9708-82ac3bc5a385" />
<img width="1920" height="1080" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/9f3e4831-2c4e-427c-b36d-479b063beaec" />
<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/8afe6c1e-25bd-4ec6-b8c4-cc304d127f65" />
<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/0d94cb0f-8572-494e-bacf-09430665c277" />
<img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/ce9c6f5f-c6b6-455d-8df2-35acf46fdc96" />
<img width="1920" height="1080" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/46de149a-90e1-4ba0-abaf-601ccc529683" />







---

All practical exercises were completed as part of the Networkwalks Internship Program.
