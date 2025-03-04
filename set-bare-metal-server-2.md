---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: set up bare metal server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Setting Up a Bare Metal Server
{: #bm-set-up}

You can set up a Bare Metal Server as a dedicated server.
{:shortdesc}

Use the following steps to set up a Bare Metal Server:

1. Log in to the {{site.data.keyword.BluSoftlayer_full}} customer portal with your unique credentials.

2. From the menu, click **Devices** > **Device list** and find your system. All of your devices are detailed in the Device List, where you can manage devices, upgrade devices, or generate bandwidth usage charts.

3. Choose to manage your server in one of the following ways:
  * Click the Device Name arrow to view a summary and manage your devices from the Snapshot view.
  * Click the Device Name of the server to view a detailed list and manage your devices from the Device Details screen.

4. Record the IP address and credentials for the server in a safe location so that you can access the details quickly without needing to log in to the Customer Portal each time you need them. You can record these details for both an individual device and for all devices associated with your account:
  * View individual device IPs from the Device List.
  * View individual device root passwords in the Snapshot View for the device.
  * View multiple device IPs by using the **Download CSV** option from the **Device List**. Then, select **Download CSV** from the **Settings** cog to download a full list of devices and details in spreadsheet format.

5. Update the credentials for operating systems and other software. All of the software that was loaded onto your device during the provisioning process was assigned temporary credentials. You can view and manage these credentials on the Passwords tab of each device in the Customer Portal. Use these temporary credentials to access your software for the first time. Then, change the password to your software by following strong password practices. Create a password that consists of a combination of letters, numbers, and symbols. Optionally, you can store password updates on the Passwords tab for each device. However, when you store passwords in the customer portal, any person with access to the account and appropriate permissions can view the passwords that are stored on the Passwords screen.

6. Access your server on the private network. You can use the {{site.data.keyword.BluSoftlayer_notm}} infrastructure private network to interact with your devices through remote desktop (RDP) by using SSH and KVM over IP. You can use the VPN Access tool for private network connection to either the closest SSL VPN endpoint or to the endpoint of your choice. VPN access is also required to interact with several services. To access the private network, edit the user’s VPN access from the User List. To access the User List, click **Account** > **Users** > **User list**. Use the [Virtual Private Network ![External link icon](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} page to connect to one of the various VPN options.

7. Set up monitoring to check the status your server and to know when to scale. You can use either standard monitoring or Nimsoft monitoring services. You can use standard, or basic, monitoring in the ping-and-respond method by using either a slow or service ping from the customer portal. You can also use Nimsoft, or advanced, monitoring from customer portal or in 1 of 3 tiers: basic, advanced, and premium.

8. Secure your system. Use the available hardware firewalls to secure your device. You can provision hardware firewalls on demand with no downtime, if rules are established properly, to protect your server from unwanted activity. After you order your firewall, it must be enabled and rules must be set.

9. Schedule backups to make sure that your data is safely stored outside of your device and able to reload any lost data. You can choose from various backup services to store your data in a secure location:
  * IBM Cloud Backup is an automated, agent-based backup system. IBM Cloud Backup is a “set-and-forget” solution for managing your device. It is compatible with Microsoft software such as Exchange and SQL through extra plug-ins. IBM Cloud Backup users interact with this service through the IBM Cloud Backup WebCC web-based application.
  * R1Soft Continuous Data Protection (CDP) can be installed on your server or self-managed virtual machine. It is recommended if you are looking for a single interface to manage all of your backups. You interact with R1Soft CDP through your proprietary management system, which allows agents to be installed on virtual machines and offers database plug-ins for extra functionality.
