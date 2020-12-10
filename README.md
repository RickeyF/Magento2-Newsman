# Magento2-Newsman

[Newsman](https://www.newsmanapp.com) module for Magento. Sync your Magento customers / subscribers to [Newsman](https://www.newsmanapp.com) list / segments. 

This is the easiest way to connect your Shop with [Newsman](https://www.newsmanapp.com). Generate an API KEY in your [Newsman](https://www.newsmanapp.com) account, install this plugin and you will be able to sync your shop customers and newsletter subscribers with [Newsman](https://www.newsmanapp.com) list / segments.
Installation

## Manual installation: 
1. Copy the *"app/code/Dazoot"* directory from this repository to your "app/code/" shop directory.

2. Edit file from *"app/etc/config.php"*

- Add these lines in the array:
 'Dazoot_Newsman' => 1,
 'Dazoot_Newsmansmtp' => 1

3. We need access to the server bash shell. And apply this command:

- ("root/yourmagentodirectory") php bin/magento setup:upgrade
```
Delete Cache 
for Magento 2.0x
```
- ("root/yourmagentodirectory/var/di") - delete di folder
```
Delete Cache 
for Magento 2.3x
```
- ("root/yourmagentodirectory/generated/metadata") - delete di folder
```
Last command
```
- ("root/yourmagentodirectory") php bin/magento setup:di:compile

## Auto installation: 
1. Copy the *"app/code/Dazoot"* directory from this repository to your "app/code/" shop directory.

2. Configuration -> Web Setup Wizard -> Module Manager -> :

Enable dazoot/module-newsman
Enable dazoot/newsmanmarketing
	
## Configuration

### Newsman Sync Addon

1. Go to **Stores > Configuration > Newsman > General Settings**
Fill in your [Newsman](https://www.newsmanapp.com) API KEY and User ID and click the Save Config button.

  ![General Settings](https://raw.githubusercontent.com/Newsman/Magento2-Newsman/master/assets/general_settings.png)

2. After the [Newsman](https://www.newsmanapp.com) API KEY and User ID are set, you can choose a list and press Save Config.

3. Choose destination segments for your newsletter subscribers and customer groups. You can choose to import customers and subscribers to a list or configure it to import in your selected segments. For the segments to show up in this form, you need to set them up in your Newsman account first.

  ![Data Mapping](https://raw.githubusercontent.com/Newsman/Magento2-Newsman/master/assets/data_mapping.png)

4. Choose how often you want your lists to get uploaded to [Newsman](https://www.newsmanapp.com) You can also do a manual synchronization by clicking "Manual Sync".

  ![Synchronization Schedule](https://raw.githubusercontent.com/Newsman/Magento2-Newsman/master/assets/synchronization_schedule.png)

5. For the automatic synchronization to work, you need to have Magento's built-in cron job functionality enabled.

### Newsman SMTP Configuration

  ![SMTP Configuration](https://raw.githubusercontent.com/Newsman/Magento2-Newsman/master/assets/smtp.png)

### Newsman Remarketing

  ![SMTP Configuration](https://raw.githubusercontent.com/Newsman/Magento2-Newsman/master/assets/marketing.png)

## Webhooks

- Unsubscribing `Newsletter Subscribers` from Magento Admin will automatically unsubscribe in Newsman List
- Unsubscribing `Newsletter Subscribers` from Newsman will automatically unsubscribe in Magento
