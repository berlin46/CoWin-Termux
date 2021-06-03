#  CoWIN Auto Booking Slot (Up : 03/06 )

Auto Slot Booking when there is a vaccine slot available at your location, by running a script on your phone. 

**If you like my work, you can support me by buying me a coffee by clicking the link below**

<a href="https://www.buymeacoffee.com/truroshan" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>        [Telegram Group](https://t.me/CoWIN_Termux)
![](https://gist.githubusercontent.com/m8rge/4c2b36369c9f936c02ee883ca8ec89f1/raw/c03fd44ee2b63d7a2a195ff44e9bb071e87b4a40/telegram-single-path-24px.svg)

https://user-images.githubusercontent.com/45506201/120487245-6bdb9300-c3d3-11eb-8983-fef996227eb9.mp4

  ## Getting Started
  By using Tremux you can run script and recieve the notification on your phone.

  - ### Install Termux 

    - Install Termux App [FDroid](https://f-droid.org/en/packages/com.termux/).
    ##### Termux wiki suggest not to use playstore termux.

    
 - ### Installing Packages and Requirements
   - Step 1 : First update pkg
    
         pkg update

   - Step 2 : Install git

         pkg install git

   - Step 3 : Clone repo 

         git clone https://github.com/truroshan/cowin-termux.git
        
   - Step 4 : Open Cloned Folder
        
         cd cowin-termux

   - Step 5: run install.sh 
         
         bash install.sh
  - ### OTP Fetching Methods
      // Three Options //
    - AutoMode (`a`) : Fetch OTP using Termux:API App 
      - Install Termux:API [FDroid](https://f-droid.org/en/packages/com.termux.api/).
          
    - SiteMode (`s`) :  Fetch OTP from Database Hosted on Cloudflare Worker
      - setup Database on [Cloudflare.](https://github.com/truroshan/CloudflareCoWinDB)
      - Install Automatically forward SMS to your PC/phone App. [Playstore](https://play.google.com/store/apps/details?id=com.gawk.smsforwarder)
    - ManualMode (`m`) : Input method

## Running Main Script for CoWin Booking

Command for script :

    python cowin.py --m <MOBILE-NO> --p <PIN-CODE> 
    
    python cowin.py --m 9966996699 --p 110011 
    
### :warning: Required values like mentioned below:

  - Replace `--m = MOBILE-NO` with your mobile no.
  - Replace `--p = PIN-CODE or DISTRICT-ID` with your Pincode or District Id.

### :bulb: Optional arguments accepted:
  - Pass `--a = YOUR-AGE ` with your age (default is 18).
  - Pass `--v = Vaccine Name` ex : cova | covi ( default any Vaccine ).
  - Pass `--d = DOSE_COUNT` Vaccine First Dose or Second Dose (default dose is 1).
  - Pass `--o` = OTP fetching mode.`a` = AutoMode `s` = SiteMode `m` = ManualMode
    ( default AutoMode )
  - Pass `--t = INTERVAL-IN-SECOND` to change the frequency of calling Cowin API  (default is 30 sec).
  - Pass `--b` for book for Today.
  - Pass `--f = Free or Paid` ( default Both Free and Paid).
  - Pass `--r` Don't use Token saved in file to re-login.
