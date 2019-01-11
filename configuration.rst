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
     /**
      * Specify main and backup SMTP servers
      */
     'hosts' => ['primaryHostName.tld', 'backupHostName.tld'],

     /**
      * Enable SMTP authentication
      */
     'smtpAuth' => true,

     /**
      * SMTP username
      */
     'username' => 'Username@mail',

     /**
      * SMTP password
      */
     'password' => '',

     /**
      * Enable TLS encryption, `ssl` also accepted
      */
     'smtpSecure' => 'tls',

     /**
      * Port
      */
     'port' => 587,

     /**
      * Name of default sender
      */
     'senderName' => PROJECT_NAME,

     /**
      * Default sender's address
      */
     'senderEmail' => 'senderMail@mail'
 ];
