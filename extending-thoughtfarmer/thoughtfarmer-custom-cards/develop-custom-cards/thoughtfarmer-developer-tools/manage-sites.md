# Manage sites

Commands used to configure remote ThoughtFarmer sites to connect to. A special identifier "default" can be used for your main development instance. Any commands without the _**--site**_ flag will use the default site.

### Add a new site

```text
grunt sites:add
```

Will ask for:

* **name**: the identifier for the site when using **--site=siteName** or just the flag **-siteName**
* **URL**: the base URL for the endpoint
* **apiToken**: Taken from the Admin panel --&gt; Api Token page.
* **applicationId**: Found in the ThoughtFarmer **Admin Panel** --&gt; **Advanced options** section &gt; **Configuration settings** page --&gt; api.ApplicationCodes setting. You can just use the "Identifier" value for "General" \(e.g. "UDFOISDDF........NFDHNW"\).

### List sites

```text
grunt sites:list
```

Shows all the configured sites.

### Delete a site

```text
grunt sites:delete --site=siteName
OR 
grunt sites:delete -siteName
```

Deletes the site with the specified name in the --site option. 

### Test a connection to a site

```text
grunt auth-test --site=siteName
OR
grunt auth-test -siteName
```

Will test the authentication with the specified endpoint. If no site specified will use "default".

