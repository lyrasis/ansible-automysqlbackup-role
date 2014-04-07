Automysqlbackup
===============

[![Build Status](https://travis-ci.org/lyrasis/ansible-automysqlbackup-role.svg?branch=master)](https://travis-ci.org/lyrasis/ansible-automysqlbackup-role)

Install the automysqlbackup utility.

---

Variables:

<table>
  <thead>
    <tr>
      <th>Variable</th>
      <th>Type</th>
      <th>Description</th>
      <th>Default</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>automysqlbackup_username</td>
      <td>string</td>
      <td>The database user that will perform the backups</td>
      <td>debian-sys-maint user</td>
    </tr>  
    <tr>
      <td>automysqlbackup_password</td>
      <td>string</td>
      <td>Password for the above user</td>
      <td>debian-sys-maint user password</td>
    </tr>   
    <tr>
      <td>automysqlbackup_host</td>
      <td>string</td>
      <td>Host name or ip address of MySQL</td>
      <td>localhost</td>
    </tr>
    <tr>
      <td>automysqlbackup_dbames</td>
      <td>string</td>
      <td>Space separated string of database names to include in backup</td>
      <td>all</td>
    </tr>
    <tr>
      <td>automysqlbackup_dbexclude</td>
      <td>string</td>
      <td>Space separated string of database names to exclude</td>
    </tr>
    <tr>
      <td>automysqlbackup_createdb_stmt</td>
      <td>string</td>
      <td>Set to "yes" or "no" for create database statements</td>
      <td>yes</td>
    </tr>
    <tr>
      <td>automysqlbackup_backup_directory</td>
      <td>string</td>
      <td>Path for backups</td>
      <td>/var/lib/automysqlbackup</td>
    </tr>
    <tr>
      <td>automysqlbackup_doweekly</td>
      <td>integer</td>
      <td>Integer to reflect weekly backup day occurence</td>
      <td>6 (Saturday)</td>
    </tr>
    <tr>
      <td>automysqlbackup_mailcontent</td>
      <td>string</td>
      <td>Command output content (log, files, stdout, quiet)</td>
      <td>quiet</td>
    </tr>
    <tr>
      <td>automysqlbackup_mailaddr</td>
      <td>string</td>
      <td>username or email address to receive mailcontent</td>
      <td>root</td>
    </tr>
    <tr>
      <td>automysqlbackup_cron</td>
      <td>hash</td>
      <td>Cron configuration for automysqlbackup</td>
      <td>*see default below*</td>
    </tr>
  </tbody>
</table>

---

Default cron configuration:

```
automysqlbackup_cron:
  minute: 0
  hour: 0
  day: "*"
  month: "*"
  weekday: "*"
```

---
