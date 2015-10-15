# Current Version #
[0.5.1](http://opendlp.googlecode.com/files/OpenDLP-0.5.1.tar.bz2) released 2012.08.27

0.5.1 Ubuntu 11.04-based VirtualBox VM released 2012.08.27

Follow OpenDLP release announcements on Twitter: http://twitter.com/OpenDLP

# Overview #
OpenDLP is a free and open source, agent- and agentless-based, centrally-managed, massively distributable data loss prevention tool released under the GPL. Given appropriate Windows, UNIX, MySQL, or MSSQL credentials, OpenDLP can simultaneously identify sensitive data at rest on hundreds or thousands of Microsoft Windows systems, UNIX systems, MySQL databases, or MSSQL databases from a centralized web application. OpenDLP has two components:
  * A web application to manage Windows agents and Windows/UNIX/database agentless scanners
  * A Microsoft Windows agent used to perform accelerated scans of up to thousands of systems simultaneously

**Web Application**
  * Automatically deploy and start agents over Netbios/SMB
  * When done, automatically stop, uninstall, and delete agents over Netbios/SMB
  * Pause, resume, and forcefully uninstall agents in an entire scan or on individual systems
  * Concurrently and securely receive results from hundreds or thousands of deployed agents over two-way-trusted SSL connection
  * Create Perl-compatible regular expressions (PCREs) for finding sensitive data at rest
  * Create reusable profiles for scans that include whitelisting or blacklisting directories and file extensions
  * Review findings and identify false positives
  * Export results as XML
  * Written in Perl with MySQL backend
  * Can deploy Windows agents through existing Meterpreter sessions (new in 0.5)

**Agent**
  * Runs on Windows 2000 and later systems
  * Written in C with no .NET Framework requirements
  * Runs as a Windows Service at low priority so users do not see or feel it
  * Resumes automatically upon system reboot with no user interaction
  * Securely transmit results to web application at user-defined intervals over two-way-trusted SSL connection
  * Uses PCREs to identify sensitive data inside files
  * Performs additional checks on potential credit card numbers to reduce false positives
  * Can read inside ZIP files, including Office 2007 and OpenOffice files
  * Limits itself to a percent of physical memory so there is no thrashing when processing large files

**Agentless Database Scans**

In addition to performing data discovery on Windows operating systems, OpenDLP also supports performing agentless data discovery against the following
databases:
  * Microsoft SQL server
  * MySQL

**Agentless File System and File Share Scans**

With OpenDLP 0.4, one can perform the following scans:
  * Agentless Windows file system scan (over SMB)
  * Agentless Windows share scan (over SMB)
  * Agentless UNIX file system scan (over SSH using sshfs)

# Intended Audience #
  * Penetration testing consultants
  * System, network, or security administrators
  * Compliance consultants

# Installation Documentation #
  * Standalone: http://opendlp.googlecode.com/files/README-0.5.1
  * VirtualBox VM: http://opendlp.googlecode.com/files/README-VM-0.5.1.txt

# Wiki Enries #
  * Regular Expressions: http://code.google.com/p/opendlp/wiki/RegularExpressions
  * FAQ: http://code.google.com/p/opendlp/wiki/FAQ

# Screenshots #
Agent-based Windows OS scan, summary results view:
![http://opendlp.googlecode.com/files/ss1-0.2.gif](http://opendlp.googlecode.com/files/ss1-0.2.gif)

Agent-based Windows OS scan, detailed results view:
![http://opendlp.googlecode.com/files/ss2-0.2.gif](http://opendlp.googlecode.com/files/ss2-0.2.gif)

Agentless Microsoft SQL Server scan, detailed results view:
![http://opendlp.googlecode.com/files/ss1-0.3.gif](http://opendlp.googlecode.com/files/ss1-0.3.gif)

# External Links #
  * Shmoocon 2011 presentation by author Andrew Gavin (discussing and demoing Windows agent scanning): http://www.youtube.com/watch?v=kz3M--LhyBg
  * Review: http://blog.rootshell.be/2010/04/30/keep-an-eye-on-your-data-using-opendlp/
  * "Dark Side" uses for OpenDLP: http://www.darkreading.com/blog/227700893/dark-side-uses-for-defensive-tools.html
  * Exotic Liability interview with Andrew Gavin: http://exoticliability.libsyn.com/exotic-liability-68-open-dlp
  * Chomp.fm interview with Andrew Gavin: http://chomp.fm/006/
  * DEFCON 2011 presentation by author Andrew Gavin (discussing and demoing agent, database, and Windows/UNIX agentless scans): https://www.youtube.com/watch?v=Xv8kbjziCds
  * DEFCON 2012 presentation by author Andrew Gavin and contributors Michael Baucom and Charles Smith (discussing Metasploit features of OpenDLP): http://www.youtube.com/watch?v=jxcaYa6fZ1g
  * Concise Courses April 2013 presentation by author Andrew Gavin: http://www.concise-courses.com/infosec/20130307/

# Future Plans #
  * Add more database support to web application to look for sensitive data at rest inside tables
  * Enhance web application interface
  * Make false positive feature more powerful and easier to use (example: mark all things as FP across all scans in file matching XYZ md5sum)
  * Add support to export results as Microsoft Word and OpenOffice documents (for those not XML-inclined)
  * Add support for performing trending analysis for different scans
  * Add ability to use Windows agent to find files matching user-specified MD5 checksums

# Downloads #
  * Standalone: http://opendlp.googlecode.com/files/OpenDLP-0.5.1.tar.bz2
  * VirtualBox VM image (1 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.001
  * VirtualBox VM image (2 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.002
  * VirtualBox VM image (3 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.003
  * VirtualBox VM image (4 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.004
  * VirtualBox VM image (5 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.005
  * VirtualBox VM image (6 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.006
  * VirtualBox VM image (7 of 7): http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.007
  * VirtualBox VM image MD5 checksums: http://opendlp.googlecode.com/files/OpenDLP-0.5.1-VM.7z.md5

# CHANGELOG #
  * http://opendlp.googlecode.com/files/CHANGELOG-0.5.1.txt

OpenDLP is copyright Andrew Gavin (andrew.opendlp@gmail.com) 2009-2012.