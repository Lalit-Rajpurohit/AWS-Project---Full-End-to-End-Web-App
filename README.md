# AWS-Project---Full-End-to-End-Web-App

**AWS Project - Build a Full End-to-End Web App with 7 Services**

Services::
<ul>
  <li>AWS IAM</li>
  <li>AWS Amplify</li>
  <li>Aws Cognito</li>
  <li>Aws Lambda</li>
  <li>Aws API Gateway</li>
  <li>Aws DynomoDB</li>
  <li>GitHub(code&files)</li>
</ul>

**Step1:**

a)Navigate to Amplify and create new app.

b)Choose GitHub for code Provider.

![Screenshot 2025-06-04 162125](https://github.com/user-attachments/assets/2a8f1675-dff3-4bf2-875d-3e2ca7569c6d)

c)Choose Repositories

![Screenshot 2025-06-04 162439](https://github.com/user-attachments/assets/48c889f5-3409-490a-ae00-14b7e7929559)

d)Save and Deploy

![Screenshot 2025-06-04 162922](https://github.com/user-attachments/assets/469630b4-3dfa-4f0e-85ce-1c773533a359)

e)use Domain link to open website in browser


**Step2:**

a)Navigate to Cognito

b)Create User Pool

c)Select Single Page Application

d)Give name ,Choose Sigin attributes and requied attributes and create

![Screenshot 2025-06-04 191353](https://github.com/user-attachments/assets/8c31fca9-dcf6-41c3-8563-d155f8457c9b)

e)Note and Copy Pool id and Client Id

![Screenshot 2025-06-04 164706](https://github.com/user-attachments/assets/ac4a6147-149a-4e4b-8540-101b4439dedc)

f) In code  of Configrution file enter pool id and client id

![Screenshot 2025-06-04 165002](https://github.com/user-attachments/assets/b668a21e-616f-4c8f-9b50-162f27a38c4b)


**Step3:**

a)from Amplify Copy Domain url run in browser

b)test Registration ,verify and  signin.

![Screenshot 2025-06-04 165224](https://github.com/user-attachments/assets/0ae3bf51-bf27-4c1f-bd03-724d4deaea96)
![Screenshot 2025-06-04 170148](https://github.com/user-attachments/assets/2189c078-4790-4767-a53f-6ec8dfd297d4)


**Step4:**

a)Navigate to DynomoDB and create table

![Screenshot 2025-06-04 170623](https://github.com/user-attachments/assets/068e544d-51a9-4b69-abc7-a803965b53ef)

b)Copy and Note ARN(Amazon Resource Name)

![Screenshot 2025-06-04 170825](https://github.com/user-attachments/assets/0cb83f98-0d08-488a-8a15-7536e17957e3)


**Step5:**

a)Navigate to IAM the create role

b)for use case choose lambda

![Screenshot 2025-06-04 171146](https://github.com/user-attachments/assets/535184ae-e283-46aa-9979-80f796468725)

c)Attach Policies(AWSLambdaBasicExecutionRole)

![Screenshot 2025-06-04 171223](https://github.com/user-attachments/assets/968a0459-7808-4517-bfab-f6df83039607)

d)Create inline Policy

e)Select Service DynamoDB and Allow actions PutItem

![Screenshot 2025-06-04 171717](https://github.com/user-attachments/assets/7e1405e9-9a87-4473-b9a0-9c5399bd7d75)

f)Add ARN of DynamoDB copied earlier(step4:b)

![Screenshot 2025-06-04 171728](https://github.com/user-attachments/assets/2205ab2a-d5e7-4639-834b-66ecbaaed934)

g)Create Policy

![Screenshot 2025-06-04 171907](https://github.com/user-attachments/assets/36b7f7ca-7ddf-4a34-b520-5a66519bb427)


**Step6:**

a)Navigate to Lambda and create function

b)Choose Author form scratch 

c)Give name and select rutime Nodejs

d)Select Existing role and choose role created earlier(step5) and create function

![Screenshot 2025-06-04 172113](https://github.com/user-attachments/assets/52279893-e5a2-45ee-9de3-91529435e401)

e) in code source in index.mjs file enter lambda code

![Screenshot 2025-06-04 172415](https://github.com/user-attachments/assets/69262fbd-618a-4d0f-b4db-875224735ac2)

f)Delploy and Test


**Step7:**

a)navigate to API Gateway and create API

b)Choose Rest API

![Screenshot 2025-06-04 173056](https://github.com/user-attachments/assets/09cb0ab9-5e99-47d8-b223-b109b0e4eb81)

c)give name and create

d)In API Dashboard Authorizers and create

e)give name and choose type Cognito

f)Select UserPool cerated earlier (Step2) and create

![Screenshot 2025-06-04 173335](https://github.com/user-attachments/assets/a06f7bc8-ff5b-44e4-88fc-a73ef1b0a418)

g)in dashborad choose Resources and create

h)give name and enable CORS and created

![Screenshot 2025-06-04 173623](https://github.com/user-attachments/assets/dc3cbe16-4e62-4620-9208-7ee902f20d72)

i)in resource select resources(/) and created method

![Screenshot 2025-06-04 173706](https://github.com/user-attachments/assets/03b7e67a-c6fc-43c9-9b3d-02181643443d)

j)Choose method type Post and Integration type Lambda Function and enable Proxy ,select lambda function and cerate function

![Screenshot 2025-06-04 173822](https://github.com/user-attachments/assets/fffc3c20-a731-46af-a0fd-f3fbdc066b37)

k) under method request settings click on edit

![Screenshot 2025-06-04 173932](https://github.com/user-attachments/assets/e753260c-f33e-4c15-a62a-d5bd2ca70d0a)

l)choose Authorization  and save

![Screenshot 2025-06-04 174002](https://github.com/user-attachments/assets/13ff1221-a710-4402-afc2-0732d6c35877)

m)Deploy API

![Screenshot 2025-06-04 174044](https://github.com/user-attachments/assets/e748014c-f4b8-4385-b212-b4c061011424)

n)copy invoke url and paste in your configuration file

![Screenshot 2025-06-04 174155](https://github.com/user-attachments/assets/84e313bb-421c-4224-9c73-29267eeff504)






    *********************************DONE**********************************************






































