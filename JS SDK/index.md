# JS API

Bonbon exposes a JavaScript API to your pages so you can 

## Event Lifecycle

Bonbon Web Tags emit JavaScript events to let the page know about various state changes during a user's visit. The first event in the lifecycle is the `bonbon::initialized` event which occurs after the page's `DOMContentLoaded` event. You can listen for this event like this:

```
window.addEventListener('bonbon::initialized', function() {
	console.log("Bonbon is initialized!");
});
```

Here is a complete list of Bonbon Web Tag events:

Event Name | Payload | Description |
---	| --- | --- 
`bonbon::initialized` | None | Fired when Bonbon has fully initialized and is ready for interaction.
`bonbon::login` | `{ detail: hashed_email: 'xxx', earn_token: 'yyy'}` | Fired whenever a user transitions from the logged out to logged in state and on every page view when a user is logged in.
`bonbon::dismissed` | None | Fired whenever a user closes a Bonbon modal.
`bonbon::opened` |  None | Fired whenever a user opens a Bonbon modal.
`bonbon::logout` | None | Fired whenever a user transitions from the logged in to the logged out state. |

## SPA

If your application is a Single Page Application (SPA), you must let Bonbon know by either <a href="">configuring your Web Tags for SPA</a> or by calling `enableSPA` after the `bonbon::initialized` event:

```
window.Bonbon.enableSPA();
```