# Incoming email

### Incoming email

An incoming email account is used by ThoughtFarmer as the entry point for all correspondence sent to the application. This is used for sending pages and attachments to the intranet as well as the [Discussion capture](discussion-capture.md) feature.  
  
The [ThoughtFarmer Service](../behind-the-scenes/thoughtfarmer-service.md) polls the inbox of this account every 10 seconds for new mail. When it finds new mail it parses the message and all attachments and adds it to the site as a new page in the appropriate section. If the message is not from a valid user or not addressed properly it will end up in the Unidentified Email section of the Administration Panel.

As a best practice the email account should not be attributed to any user within ThoughtFarmer and should not be used for any other purpose. This will prevent spam and email loopbacks from coming in.

**Go to:**

* [Configuring incoming mail](incoming-email.md)
* [Mail server type](incoming-email.md)
* [Exchange mode](incoming-email.md)
* [Mail ports](incoming-email.md)

### Configure incoming mail <a id="section1"></a>

1. Go to the **Administration panel**: **Notifications** section &gt; **Incoming mail** page.
2. Click **enable** to allow you to enter the following configuration information:![7.1Admin10519EnableIncomingMail.jpg](https://community.thoughtfarmer.com/imagethumb/44437330000/16406/950x950/False/7.1Admin10519EnableIncomingMail.jpg)
   1. **Email Address**: The incoming mail account's address.
   2. **Mail server type**: One of Exchange, IMAP, or POP3. The type of protocol used to connect to the mail server.
   3. **For Exchange mail server type**:
      1. **​URL**: The name of the incoming mail server in URL format \(eg. http://mail.exchangeserver.com/Exchange\)
   4. **For IMAP or POP3 mail server type**:
      1. **Incoming Mail Server**: The name of the server \(e.g. imap.mailserver.com\).
      2. **Port**: The proper port for the configured protocol \(see [mail ports](incoming-email.md) for a list of common port values\).
      3. **SSL**: Check the box if SSL is required on the mail server.
   5. **Username**: The login name for the incoming mail account. In Exchange mode this will be in Domain login format DOMAIN\userName.
   6. **Password**: The corresponding password for the account.
3. Click **Save changes** to apply the changes.
4. Return to the incoming mail page and click **Test Connections**.
5. Click **Verify**. Any errors in connecting or logging on will be presented in the test results.

Once both tests are successful the incoming email will be fully configured and operational.

### Mail server type <a id="section2"></a>

ThoughtFarmer supports three types of mail server connections. POP3, IMAP, and Exchange. IMAP and POP3 are standard mail protocols available on most mail servers. Exchange servers can have these services configured and enabled for connection. Exchange servers also allow for connectivity using WebDAV. Configuring this will allow you to use the Exchange mode in the mail server type.  
 

### Exchange mode <a id="section3"></a>

Exchange mode utilizes WebDAV in order to access the Exchange server. In order for this to work with ThoughtFarmer WebDAV needs to be enabled on the Exchange server. Additionally, the web instance created by Exchange for this \(by default the URL is http://mailserver.domain.com/Exchange\) needs to have Integrated Windows Authentication enabled.  
  
In the Exchange 2007 Management Console go to **Server Configuration** &gt; **Mailbox** &gt; **WebDav** &gt; then select properties on the site titled **Exchange**.  
  
![](https://community.thoughtfarmer.com/imagethumb/835989170000/16405/386x425/False/Exchange+settings.png)  
  
Note that WevDAV is not compatible with Exchange 2010, so the above steps are not necessary.

### Email ports <a id="section4"></a>

When you first configure the Incoming mail choosing the **Mail server type** will automatically set the appropriate port. It may not update the port if you change the server type again. Please verify the port settings on your mail server to assure no errors.  
  
The default ports for the mail server types are:

* POP3 - port 110
* IMAP - port 143
* IMAP4 over SSL \(IMAPS\) - port 993
* Secure POP3 \(SSL-POP\) - port 995

