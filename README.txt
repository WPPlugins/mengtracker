=== MengTracker for Wordpress ===
Contributors: menguzar, culdesac
Donate link: http://www.keditasmasi.com/mengtracker-for-wordpress/
Tags: stats, links, outgoing
Requires at least: 2.0.0
Tested up to: 2.1
Stable tag: 1.0.0b

MengTracker is a click-tracking system. It shows clicked links, clicking place of the links, and the clicking time. All with pretty charts ;)

== Description ==

The latest information about this plugin can be found at: http://www.rebitran.com/mengtracker-for-wordpress

Analysis?

When the plugin is activated, a "MengTracker" page will be added under the "Links" tab of your Wordpress admin panel. Everything is here.

First time you see the analysis screen, what you see will be the last 100 clicks from all regions on your site.

Last Clicks:
Last Clicks

In this table, "Site" shows the outbound link, "Page" shows where it is clicked from, "Region" shows the region where the link was on the page (read more about regions below), "IP" shows the visitor's IP and "Time" shows the time of the click.

When you click the "Site" link, you'll access detailed information about the link -according to your filters), when you click on the IP link, you'll access the IP lookup page from dnsstuff. [To change the IP Lookup page, see the settings section.]

Sites:
sites_s.jpg

In this tab, you'll see the most visited sites linked from your site. This counts the links by grouping them according to their domain names. It means that www.keditasmasi.com/kofti and www.keditasmasi.com/tenekeli-kuyruk, are counted as "keditasmasi.com".

Pages:
Pages

In this tab, you'll see the most visited pages linked from your site. It counts the clicks without any grouping.

Clicked Regions:

clickedregions_s.jpg

In this tab, you'll see the most popular regions on your site. When you click on the region name, it filters the results to show only the clicks from that region.

Clicked Pages:
clickedpages_s.jpg

In this tab, you'll see the referring pages of your links.

Filters:
You can filter your statistics in 3 ways.
- Date Interval: "today", "yesterday", "last 7 days", "7-15 days ago", "this month", "this year" and "all times".

- Regions: MengTracker comes with 3 default regions: "post", includes the links in your posts' texts, "comment" includes the links in your comments' texts and "commentauthor" includes the links in the comment authors' URLs. To add new regions, please check the "link code" section below.

- Limit: The statistics are always ordered from the most clicked to the least clicked links (I will add customizable ordering in the later versoins) and this filter, defines the number of rows to list. Default options are "top 10", "top 50", "top 100" and "All".

Settings:
There are 3 different settings:
settings_s.jpg

Language: Lets you choose the MengTracker administration interface. For more information on language packs, see the section below.
IP Lookup Page: Defines where to go for the IP Lookups when you click on the IPs in the statistics. The default is dnsstuff's IP Lookup page. If you want to change it, you can enter an URL with the IP as its last parameter. For example I'm sending the IPs to the IP history page of my statistics program (twatch).
Don't count internal links: Defines whether the links beginning with your domain name will be included in the statistics or not. The default is only counting the outbound links.

== Installation ==

- Download the zip file [mengTracker-1.0.0-en.zip (65,8k)]
- copy the mengtracker directory under your plugins directory.
- Activate the plugin.
- According to your server configuration, you may need to change the permission of mengtracker/ampie. If you get a "permission denied" error, send these commands from your FTP client.
chmod 777 chart1.txt
chmod 777 chart2.txt
chmod 777 chart3.txt
chmod 777 chart4.txt
- You're done.

How does it work?

When you activate the plugin, MengTracker installs itself to every data-driven item on your blog (like posts, comments...) and starts counting the clicks on your links.

It does this by adding an "onmouseup" event handler to all your links automatically when showing them.

Adding the Link Code Manually:
For occasions when your content is not generated automatically (i.e. the links you add manually to your sidebar or header), to track those links, you can change your links' code as shown below:

Your Link Code:
<a href="http://www.keditasmasi.com">Kedi Tasmasi</a>

Modified Code:
<a href="http://www.keditasmasi.com" onmouseup="javascript:mengTracker('region_name',this.href);">Kedi Tasmasi</a>

The "region_name", defines the originating region of the click.

There's nothing special to do to add a new region. You can write anything you want for the "region_name" parameter in the code above. After the first click on that link, this region will be included in the result filters on your administration panel.

Language Packs:

You will find language pack files in the "languages" directory in the zip file. The default is "english.php". You can translate the contents of the file to any language you want, rename the file, and you'll have MengTracker in your language when you select your language file from the settings.

Download:

mengTracker-1.0.0-en.zip (65,8k)

Known Bugs:

- If the texts in the charts are too long, they may overlap. Since we've used amCharts for the charts, for now, this has no ready solution.

To do:

- Add paging to "last clicks"
- Change the main filter code to something suitable for behaviour.js

HISTORY

2/1/2007
- Thanks to Ferca network team, Spanish language support is added

v1.0.0 beta (1/1/2007)
- added charts
- admin panel redesigned
- added settings
- added language support
- added IP Lookup Page customization
v0.1.0 (1/12/2006)
- tracker code
- simple stats
- adding regions