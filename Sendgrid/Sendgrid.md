# Reading 33: Sendgrid

# SendGrid

## What is SendGrid?
SendGrid is a cloud-based email service. It provides a lot of functionality such as sending receipts or confirmations to 
customers, administering an email list, forwarding/processing incoming emails, and collecting data an metrics overall 
pertaining to emailing. A default free account for SendGrid through Azure allows for 25,000 emails to accessed a month.

## Signing Up
After signing in to an existing Azure account, under the `Resources` tab, you can select SendGrid (may require a manual 
search). After clicking on it you should be able to create and account and sign in. After choosing a plan and confirming 
the purchase (can be free), you will be presented with the main page with the ability to `Manage` it.

## Using SendGrid
First you need to download the NuGet package for `Sendgrid` by Elmer Thomas and make sure the appropriate files are 
`using SendGrid` and `using SendGrid.Helpers.Mail`. `new SendGridMessage()` creates what will end up being an email. 
There are many properties for this object that correspond to common parts of the typical email. For example, there is 
`Setfrom` for the sender, `AddTos` for a list of recipients, the `SetSubject` containing the subject and lastly the data 
which can then be defined with the proper `MimeType`. The email, now full of content, can be send using a client 
configured with the API key from you SendGrid account: `var client = new SendGridClient(apiKey)` and then 
`var response = await client.SendEmailAsync({email})`. SendGrid offers even more options such as attachments, 
footers, and click trackers.