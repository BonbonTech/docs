# Getting Started

<script>
	document.getElementsByTagName("html")[0].classList.remove("dark")
</script>

Bonbon helps content creators <i>connect</i> and <i>engage</i> with their audiences through a suite of customizable tools that deliver real business impact with ease.

## Bonbon Web Tags

Bonbon Web Tags are installed on websites and offer out-of-the-box ways to reward users for their engagement.

### Installation

To add Bonbon Web Tags to your site, get your client ID from your Bonbon Account Manager and then drop this tag in the `<head>` of your pages (or in your tag manager):

```
<script>
function bonbontag(){bonbonDataLayer.push(arguments);};(function(w,d,s,l,i,e){w[l]=w[l]||[];w[l].push({'bonbon.start':new Date().getTime(),event:'bonbon.js'});var f=d.getElementsByTagName(s)[0],j=d.createElement(s);j.type="text/javascript";j.async=true;j.setAttribute('data-clientId',i);e&&j.setAttribute('data-environment',e);j.id='bonbon-js-sdk';j.src='https://cdn.bonbon.tech/js/bonbon.js';f.parentNode.insertBefore(j,f);})(window,document,'script','bonbonDataLayer','[YOUR_CLIENT_ID]');
</script>
```

<!-- ### Configuration & Activation

Activate your Bonbon Web Tags by logging into https://portal.bonbon.tech using an email address from the domain where you just installed the tags. So if you installed the tags on bonbon.tech you'll need to sign into the portal using an @bonbon.tech email address to activate the tags.

Once logged in, you'll pick your configuration, sign the TOS and confirm activation.

Once activated, your Web Tags will start serving offers using your selected configuration.

### Customizing User Journeys

Learn how to customize user journeys using our UI components in the next section. -->