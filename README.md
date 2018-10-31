# emis-investigation-follow-up
A system of protocols and searches to assist in ensuring tests and two week wait referrals that a clinician requests are followed up

!This system is still in beta testing!

There are two parts to this system
  1) "Follow up" protocol - this is the protocol the user runs when requesting a test. It adds a diary entry and a code to the notes to mark the time when the test was requested and the time when it is due. The protocol can be triggered from the F12 launcher, but also triggers automatically if a user enters the code "follow up" in the notes
  2) "Follow up checker" protocol - this protocol runs in the background every time the patients record is loaded. It checks for outstanding diary entries and completes them if the test has already been done. It also produces an alert to ask clinicians/reception to remind the patient their test is due. 

There are also two searches with associated reports. 
  1) Investigation follow up - In our practice a member of the admin team runs the "Investigation Follow Up Search" once a week and sends out reminders to the patients who have not had their tests. If they do not respond then the admin team send a task back to the clinican who requested the test. 
  2) 2 week wait follow up - we run this once a month. The report helps identify if the patient has had a letter relating to the referral. However, sometimes manual checking of the notes is required. 
  
Potential issues:
- code and diary entry conflicts. If you are already using these diary entries or codes for something else then that may result in a conflict - existing diary entries may be completed automatically for example. 
- different conding of test results. If in your area a result such as bilirubin is coded using a different code to that used in our area then the protocol may not pick up that the test has been done. You may need to alter the code it is looking for in the investigation "Follow up checker" protocol
