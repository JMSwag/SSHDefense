SSHDefense
==========
SSHD defense &amp; monitoring utility for GNU/Linux
author:  ohdae (ams) - 2013
website: https://github.com/ohdae/SSHDefense

Description
===========
This utility is used to monitor SSHD activity logs for
suspicious actions and events. By running this script as
a daemon, it will continually monitor your logs for certain
events and keywords which might indicate unauthorized access attempts.

Monitoring Modes:
* 'monitor' - log only
  monitor mode simply watches the incoming log events
  and saves suspicious alerts to a custom log file for
  later review. no actions other than logging will be taken.

* 'alert' - log and alert
  alert mode incporates 'monitor' but also can be set to
  send email, text message, growl or tty alerts when suspicious
  events occur. you will be actively informed of all incoming and/or
  on-going security events.

* 'active' - log, alert, drop, collect
  active mode performs all of the above actions from
  'alert' mode but is also used to actively block the
  suspicious IP addresses involved in each alert. IPTables
  is used to drop all traffic from the attacker host.
  A report document is also created with detailed information
  on the events that caused the alert action, as well as
  information on the attacker host itself such as whois, dns
  lookups and actively search other service logs in an attempt
  to find other events from the same attacker host.
