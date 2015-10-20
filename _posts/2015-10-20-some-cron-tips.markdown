---
published: true
title: Some cron tips
layout: post
---
* Absolute path to executable (since env may not contain PATH)
* Test with sh instead of bash
* Ensure the file is executable
* Ensure cron is installed and running (pgrep cron)
* In some systems (Debian, Ubuntu) logging for cron is not enabled by default. In /etc/rsyslog.conf or /etc/rsyslog.d/50-default.conf uncomment the line:

	# cron.*                          /var/log/cron.log

  After that, you need to restart rsyslog via
	/etc/init.d/rsyslog restart
  or
	service rsyslog restart
* Executable file in /etc/daily.d or hourly.d needs the hashbang #!/bin/bash
