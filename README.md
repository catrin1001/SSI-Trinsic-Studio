# Issue and Verify digital credentials
This document will walk through a scenario where Ceit will receive a college diploma and prove to her employer she graduated college to get a job.


## Create Organizations

1. Go to the Trinsic Studio and log in.
2. Click on the + Organization, and create an organization called "George Brown College" on the Sovrin Staging Network.
3. Repeat Step 2 for a second organization called "RBC Bank".

## Create credentials
Ceit will receive her transcript from George Brown College in a digital format. In order for that to happen, George Brown college has to setup a template. 

1. Click on the **George Brown College** organization card to enter into the organization. 
2. Go to the **Credentials** tab and click the **Create Template** button. 
3. Using the **New Schema** tab, name the credential "College Transcript" and add these three attributes:
    - Full Name
    - Degree
    - Year
4. Click **Continue to Review** and the **Confirm**. There will be a 1-3 second delay while the template is written to the ledger.
5. Copy the credential's Schema ID for later

## Install Trinsic Wallet
Download the Trinsic Wallet for iOS or Android.

## George Brown College issues a transcript

1. Navigate to the **Credentials** tab in the George Brown College Organization in the Trinsic Studio.
2. Locate the "College Transcript" credential template.
3. Click on the **Offer** icon that corresponds with that template.
4. Fill in all the attributes with Alice's information, then send the credential via **Create Offer Link**.

## Create a connection with RBC Bank

The first step to create a connection is to send an invitation. Connection invitations are usually transmitted through QR codes or deeplinks.

AS RBC Bank:
1. Click on the **RBC Bank** organization card to enter into the organization. 
2. Go to the **Connections** tab and click the **Invite Connection** button. 
3. Click the **Generate Invitation** button.
4. You should see a QR code appear in the panel. You can scan the QR code, send it via email to someone, or copy the URL.

Now, as Ceit:
1. Open your mobile wallet app and tap on Scan Code.
2. Scan the QR code that is displayed in Trinsic Studio.
3. When the connection invitation shows up in the wallet, tap ACCEPT.
The connection will be added to your wallet.

## Create RBC Bank job application
Now that Ceit has her first credential, she can begin to use it to prove things about herself. In this case, she wants to get a job and can use her digital college transcript to do so.

RBC Bank can create a job application using a Verification Template

We will assume that RBC Bank requires the following things to hire Ceit:
- Full Name
- Degree
- Year


1. Click on the Dashboard and go to the **George Brown College** organization. 
2. Click on the **Credentials** tab.
3. Click on the **information** icon
4. Copy the **Schema ID** from the College Transcript credential template

Now create the Job Application template:

1. Click into Dashboard and go to the RBC Bank organization.
2. Click on the **Verifications** tab and click the **Create Template** button. 
2. Name the verification "Job Application".
3. Click on the **+ Credential Request**.
4. Enter "Transcript Verification" as the "Requested Credential Name".
5. In the **Attribute Name** textbox, enter the attribute names exactly as they appear in the credential template that you created for Faber College.
6. In the **Advanced** dropdown, select **Schema ID** and paste the transcript Schema ID into the textbox that appears. This is so that only credentials issued from the template you created previously will pass the verification. 
7. Click the **Create** button and wait a few seconds for the template to be saved.


## RBC Bank Sends Ceit a Job Application
Now that RBC Bank has set up its verification template, it can send its verification to Ceit!

As RBC Bank:
1. Click on the **Connections** tab in the RBC Bank organization in the Studio.
2. Locate the connection you'll use to request a verification from Ceit. Click on the **blue checkmark** icon which corresponds to this connection.
3. Click the **Request Verification** button towards the bottom of the screen.
4. Select the "Job Application" from the list of templates.
5. Click **Send Request**

Now as Ceit:
Your Trinsic Wallet should get a push notification for the verification request from your RBC Bank connection.
From your home screen, select the verification request to respond. Once you've opened it, you can customize the information you share if you have more than one credential that can satisfy the request.
If the information looks correct, press ACCEPT.
