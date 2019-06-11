# Securing ThoughtFarmer



### Securing ThoughtFarmer

ThoughtFarmer comes with a set of security features enabled by default to prevent potential attacks from malicious users. These include:

1. **Request Validation**: All field and form data is checked on submission for values that could be used in an attack \(e.g. script, html, etc.\). If any is found the application will throw an error and prevent the data from being triggered. This is to prevent [Cross Site Scripting \(XSS\)](http://en.wikipedia.org/wiki/Cross-site_scripting) attacks.
2. **Anti-forgery Token**: All requests made to the server utilize an anti-forgery token. This allows the application to be sure requests are coming from a valid user and not a malicious source, preventing [Cross Site Request Forgery \(CSRF\)](http://en.wikipedia.org/wiki/Cross-site_request_forgery) attacks.

While the above security filtering has a minimal impact on users, some security settings may cause a reduction in functionality or performance. Because ThoughtFarmer is designed to run internally within an organization, some higher security options have been disabled in recognition of this trade-off.

  
External Access

If ThoughtFarmer is available outside your internal network \(e.g. accessible over the Internet without a VPN connection\) you may wish to take additional steps to secure the server. The following security measures are available to harden ThoughtFarmer further, albeit with some trade-offs for performance and functionality.

1. Use an SSL certificate to encrypt data sent to and from the server / client. See Enabling SSL for more info. Note: due to the overhead with SSL, this may reduce performance slightly.
2. Use the [Enhanced Security Filter Set](../customize-your-content/rich-text-editor/filter-content.md) for the Rich Text editor. This will perform very strict server-side XSS filtering for all HTML content. Note that this may disable the ability to embed some rich functionality \(E.g. Wistia video embeds\).
3. Under [Attachment Settings](attachement-settings.md), change the permitted extensions to "Only Allow..." and enter only "safe" attachment extensions \(e.g. "doc,docx,xls,xlsx,ppt,pptx,pdf,jpg,png,gif" etc.\).
4. Use Windows Integrated Authentication for configuring the application to connect to the database.
5. Restrict access to the web services to specific IP Addresses. The file ~/Services/CacheWebService.asmx can be limited in IIS to only be accessible from the web server itself.

