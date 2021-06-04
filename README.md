# Captive-portal
An open source Captive portal for use with Ubiquiti external captive portal tool

# Reason
I was looking through my UDM (Unifi Dream Machine) and discovered the guest hotspot which allows you to create a wireless access point for others to join with captive portal. the cool part about this was the payments method which could allow you to charge for usage, this is nothing new but i felt like something was missing in the payment options. Bitcoin. UI gives us several payment options out of the box but wouldnt it be nice to have an option to accept bitcoin, so i will now make an custom web portal (fresh ubuntu machine) which allows you to link a BTCpay server to it and start making money. (Past me PLEASE EDIT LATER IN PROJECT THIS SUCKS)

# How this will work, I think?
1. User will choose access point in wifi
2. UDM will route the incoming request to a local vm, raspberry pi or external server
3. The VM will log ip of device and mac to a mariadb database which will check if User has accessed service before, how long they have used service, how much data (?), etc
4. After Vm finds or creates the User it will redirect to correct page by nginx
5. Database will log all usage and create time records
