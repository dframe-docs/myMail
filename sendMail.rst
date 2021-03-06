.. title:: MyMail - sending emails

.. meta::
    :description: MyMail - sending emails
    :keywords: php, mailing, php, php7, send mail, buffer, queuing, smtp, imap, mail wrapper, dframe

The library can be used independently, that means you don't need a framework. Access to the phpMailer class is through the |mail| variable. The code below is an example of sending the email to the receiver instantly.

.. code-block:: php

 use Dframe\MyMail\MyMail;
 
 require_once __DIR__ . '/../vendor/autoload.php';
 $config = require_once 'config/config.php'; 
 
 $MyMail = new MyMail(); // Załadowanie Configu
 $MyMail->mail->isSMTP();
 $MyMail->mail->SMTPOptions = array(
     'ssl' => array(
         'verify_peer' => false,
         'verify_peer_name' => false,
         'allow_self_signed' => true
     )
 );
 //$mail->SMTPDebug  = 2; // enables SMTP debug information (for testing)
                        // 1 = errors and messages
                        // 2 = messages only
 $MyMail->mail->SMTPSecure = false;
 
 $addAddress = array('mail' => 'adres@email', 'name' => 'titleFrom'); // Adresy na jakie ma wysłać
 
 try {
     $MyMail->send($addAddress, 'Test Mail', $body);
 
 } catch (Exception $e) {
     echo $e->getMessage();
     
 }

.. |mail| cCode:: $MyMail->mailObject 
