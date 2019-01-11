.. title:: MyMail -  Sendmail Wrapper 

.. meta::
    :description: MyMail - wrapper for send mail - dframeframework.com
    :keywords: php, mailing, php, php7, send mail, mails, smtp, imap, mail wrapper, dframe

Instalation
----------

From console level, launch the command composer* 

.. code-block:: bash

 $ composer require dframe/mymail

Or download manual https://github.com/dframe/mymail/releases

The myMail library is a simple wrapper, this time for phpmailer. In a simple way, you can set data for connection in config.

.. code-block:: php

 return [
     'Hosts' => ['primaryHostName.tld', 'backupHostName.tld'],    // Specify main and backup SMTP servers
     'SMTPAuth' => true,    // Enable SMTP authentication
     'Username' => 'Username@mail',    // SMTP username
     'Password' => '',    // SMTP password
     'SMTPSecure' => 'tls',    // Enable TLS encryption, `ssl` also accepted
     'Port' => 587,    // Port
 
     'SenderName' => PROJECT_NAME,    //Name of default sender
     'SenderEmail' => 'senderMail@mail'    //Default sender's address
 ];
