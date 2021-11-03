---
order: 2
pcx-content-type: reference
---

# Email Routing options

Email Routing is under Email in the Cloudflare dashboard. It is divided into four sections:

* Custom address rules
* Catch-all
* DNS
* Verified emails

## Custom addresses

In this section you can create as many custom email addresses as you want for your domain. Each of those custom addresses is then linked to a destination address, forming a **rule**. Rules can be toggled on or off.

To create your rule, you also have to specify an **Action** between the email alias and the destination address:

* **Send to**: emails will be routed to your Destination address. This is the default action.
* **Drop**: Accepts emails but deletes them without routing to the specified Destination address.This can be useful if you want to make an email address appear valid for privacy reasons.

<Aside type="note">

All rules are automatically disabled until the destination address is validated by the user. This is to prevent spamming unintended recipients. 

</Aside>

## Catch-all address

This feature enables Cloudflare to “catch” every variation of emails, in order to make them valid for the specified domain. For example, if you created a rule for `john@yourdomain.com` and a sender accidentally types `jonh@yourdomain.com`, the email will still be correctly handled if you have Catch-all addresses enabled.

You must also specify an **Action** to Catch-all:

* **Send to**: emails will be routed to your Destination address. This is the default action.
* **Drop**: Accepts emails but deletes them without routing to the specified Destination address.This can be useful if you want to make an email address appear valid for privacy reasons.

## Email DNS records

All DNS records needed for Email Routing are shown and can be added automatically here, if not yet fully compliant. This is also where you can confirm if there are any conflicts that may result in unexpected behaviors.

## Verified emails

In this section there is a list of Destination addresses that have already been verified. This is also where you can resend a verification email, or delete Destination addresses.

Email Routing rules do not become active until after the destination address has been verified. Cloudflare sends an email to every Destination address you specify in Custom addresses. You have to click **Verify email address** in those emails before a Destination address can be used.

<Aside type="note">

Deleting a Destination address automatically disables all routing rules that use that email address as destination.

</Aside>