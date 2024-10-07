# Widgets

<script>function bonbontag(){bonbonDataLayer.push(arguments);};(function(w,d,s,l,i,e){w[l]=w[l]||[];w[l].push({'bonbon.start':new Date().getTime(),event:'bonbon.js'});var f=d.getElementsByTagName(s)[0],j=d.createElement(s);j.type="text/javascript";j.async=true;j.setAttribute('data-clientId',i);e&&j.setAttribute('data-environment',e);j.id='bonbon-js-sdk';j.src='https://cdn.bonbon.tech/js/bonbon.js';f.parentNode.insertBefore(j,f);})(window,document,'script','bonbonDataLayer','h1BcGIlUGgflboYmUIC7JTa3OlA75QG8');
</script>


## The Rewards Widget

The `<bonbon-rewards>` widget offers a rewarding experience for your users that drives engagement & registrations. `<bonbon-rewards>` uses the site, site section & page context to deliver a relevant prize offer, quiz and/or poll that delivers incremental time on site, ad viewability & optimizes conversion to an addressable user in a 3rd party cookieless world.

The widget can be rendered inline like so:

```
<bonbon-rewards></bonbon-rewards>
```

Renders:

<div style="padding: 12px; background: #e1e1e1;margin-bottom:24px;">
	<bonbon-rewards></bonbon-rewards>
</div>

`<bonbon-rewards>` can be configured to show automatically in a modal based on a variety of combinatorial targeting factors including:

* Single session article view depth
* Cross session article view depth
* Country
* Page URL Match (regex)
* Custom parameters (talk to your Account Manager)

Or you can trigger the modal directly using our JS SDK by calling:

```
window.Bonbon.openModal({component: 'bonbon-rewards'}).load();
```

<a href="javascript:Bonbon.openModal({component: 'bonbon-rewards'}).load();">Click here to see Bonbon Rewards load in a soft modal</a>



## AdWall

The `<bonbon-ad-wall>` widget is intended to be rendered in a modal and can be configured as a hard or soft gate. A hard gate would require the user to watch a short video ad or register to get access to content for a configurable dimension e.g. 4 hours, 3 days, 4 articles, 4 sessions.

The modal can be configured to show automatically based on a variety of combinatorial targeting factors including:

* Single session article view depth
* Cross session article view depth
* Country
* Page URL Match (regex)
* Custom parameters (talk to your Account Manager)

Or you can trigger the modal directly using our JS SDK by calling:

```
window.Bonbon.openModal({component: 'bonbon-ad-wall'}).load();
```

<a href="javascript:Bonbon.openModal({component: 'bonbon-ad-wall'}).load();">Click here to see the Bonbon Ad Wall load in a soft modal</a>


## Leaderboard

The `<bonbon-leaderboard>` widget shows the top 100 users by their earned engagement points.

```
<bonbon-leaderboard></bonbon-leaderboard>
```

<div style="max-height: 300px;overflow-y: scroll;margin-bottom:24px;">
	<bonbon-leaderboard></bonbon-leaderboard>
</div>

## Login Button

The `bonbon-sso-button` custom element can be used to let users know they can login to their Bonbon account.

```
<bonbon-sso-button></bonbon-sso-button>
```

Renders the Bonbon SSO Button:

<div style="width:300px;">
	<bonbon-sso-button></bonbon-sso-button>
</div>

<bonbon-offer-grid></bonbon-offer-grid>

