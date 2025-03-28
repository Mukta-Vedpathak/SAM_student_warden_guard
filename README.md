# SAM_student_warden_guard
1. Current Process:
● Students planning to travel out of the station must obtain an out pass from the hostel guards. They
should fill in the required details and get the wardens to sign it.
● The out pass must be submitted to the respective hostel managers at least one day before the journey
to allow enough time for the warden’s signature during office working hours. Wardens need to visit
the hostel to sign the passes, which involves paperwork.
● After receiving approval from the wardens, the student must have the out pass checked by the guard
at the hostel gate. The student is also required to enter their details (name, roll number, contact
number, year, branch, etc.) in the register at the gate.
1.1. Issues in the current process:
● Students do not carry their ID cards with them or do not make entries in the register.
● The bus carrying students often waits at the gate for an extended period while students fill
in the details.
● Sometimes, a large crowd of students causes delays, and some students may not complete
the entry.
● This time-consuming process creates coordination challenges for students, guards, and
wardens. A more efficient solution is needed to streamline this process.
2. App Overview and Workflow:
To address the inefficiencies in the current out-pass process, we developed a solution: SAM (Security
Application Module)
There will be 3 web apps: Student, Warden, and Guard.
2.1 Student Portal:
● Students log in with a unique Roll number and LDAP password.
● The student dashboard displays their outing request history, including the warden’s
approval status and remarks.
● Students can submit a new outing request by providing the reason for leaving, the out
date, the in date, and any necessary documents or attachments (optional).
2.2 Warden Portal:
● Wardens log in with a unique username/email and password.
● They can view all outing requests on the dashboard, approve or reject them, and add
remarks.
● Remarks can be entered manually.
2.3 Guard Portal:
● When the student is leaving the hostel, guards must scan the QR code on the ID-card of
the student.
● Student details and warden approval information will be displayed for verification, and
the out time will be updated in the database immediately after scanning.
● When the student re-enters the hostel, the guard will scan the QR code again, and then in
time will be recorded.
Benefits:
● Reduces paperwork
● Eliminates the need for wardens to visit the hostel for approvals.
● Makes entry and exit faster as guards can mark the times with a single scan.
● Students will have to carry their ID cards compulsorily.
3. Workflow Diagram:
4. Installations & Requirements: (Ubuntu Recommended)
● Flutter: https://www.youtube.com/watch?v=32uMbzEt49s
● $ pip install -r requirements.txt
5. Directory Structure & Instructions to Run the App:
DevHack6.0_Athena
|---backend
| |--app.py
| |--credentials.json
|---student_frontend
|---warden_frontend
|---guard_all
|---requirements.txt
To run the app(in Ubuntu), open 4 terminals and run the following commands parallelly.
1) $ cd DevHack6.0_Athena/backend/
$ python app.py
2) $ cd DevHack6.0_Athena/student_frontend/
$ flutter clean
$ flutter pub get
$flutter run -d chrome
3) $ cd DevHack6.0_Athena/warden_frontend/f
$ flutter clean
$ flutter pub get
$flutter run -d chrome
4) $ cd DevHack6.0_Athena/guard_all
$ python app.py
Open the http link in a web browser from the terminal.
Sample Login Credentials: (refer to database for more options)
Student Portal: LDAP ID=test_id, Password=pass
Warden Portal: EMAIl ID=hos1girls@iitdh.ac.in, Password=34
Guard Portal: Username=admin, Password=password
6. Video Demo:
https://drive.google.com/file/d/1EnPtc7b0b6zsTkCrfoKLNNZDIvd2kAcF/view?usp=sharing
(Detailed Demo)https://drive.google.com/drive/folders/1sexD2L9UGuRgsTPVAFIowL7VzuX9XnS7.Database(Google Sheet):
https://docs.google.com/spreadsheets/d/1oSdzxFI67ZPRMM_EHfIo_Mcquh35iPNpfXkAj6N96T0/edit
?usp=sharing
8. Technologies used: Flutter, Flask, Python, HTML, CSS, Javascript, Google Sheets API, QR code
scanner, Docker, Netlify, Ngrok.
Docker container: https://hub.docker.com/r/flameop12/security_host
