# Contact-Form

This project contains serveral HTML contact forms using a Bootstrap framework and AJAX with PHP. 

PHP Scripts are used to handle data and send emails.

JavaScript magic (jQuery) is used to submit the form via AJAX without reloading the page itself. 

The end result of this project are responsive contact forms with validation fields and with some basic CSS styling.

<h2>HTML</h2>

The HTML layout of the contact form includes:

* Within the <b>head</b> tags there is a bootstrap stylesheet for Google fonts, and a <b>custom.css</b> stylesheet.
* Before the <b>body</b> end tag there are several javaScripts(jQuery &amp; Bootstrap) and a contact.js file that includes AJAX.
* The empty <b>div</b> with <i>class="messages"</i> is use to display error messages.
* Bootstrap validation is used to help the UI on HTML forms - attributes such as <i>type="email"</i> &amp; <i>type="tel"</i>.
* Within the <form> tag we use several attributes:<br/> 
&ensp;&ensp;&ensp;-> <i>id="contact-form"</i> is use to identify the form.<br/>
&ensp;&ensp;&ensp;-> <i>method="post"</i> is use to send the contact form values.<br/>
&ensp;&ensp;&ensp;-> <i>action="contact.php"</i> is use to call the PHP script.<br/>
  
<h2>PHP</h2>

The contact.php file is the PHP script that handles sending emails. This file includes:

* <b>$from</b> - represents the email address that will be in the From field of the email.
* <b>$sendTo</b> - represents the email address that will receive the email. 
* <b>$subject</b> - represents the subject of the email.
* <b>$fields</b> - an array of form control names and their counterparts.<br/>
&ensp;&ensp;&ensp;-> For example: an input called name <i>(input name="name")</i>, can be like this: <i>'name' => 'Customer Name'</i>
* <b>$okMessage</b> - represents the message text displayed on the web page.
* <b>$errorMessage</b> - represents the text of the error message displayed.

<h2>PHPMailer</h2>

<a href="https://github.com/PHPMailer/PHPMailer">PHPMailer</a> is a full-featured email sending library for PHP. 

Within (<i>contact-2.php &amp; contact-2.php</i>), <a href="https://github.com/PHPMailer/PHPMailer">PHPMailer</a> email-sending library replaces the standard and basic PHP mail() function. 

<h2>JavaScript</h2>

The JavaScript within the forms handle the validation and email sending via AJAX. The <b>contact.js</b> includes:

* <b>POST</b> request to the <i>contact.php</i> script when the <i>#contact-form</i> is submitted.
* <b>JSON</b> object is returned by the <i>contact.php</i> script. The object has only two properties - <i>type &amp; message</i>
* <i>type &amp; message</i> is used to contstruct the message -<br/>
&ensp;&ensp;&ensp;-> <b>alert-danger</b> for errors.<br/>
&ensp;&ensp;&ensp;-> <b>alert-success</b> for success.<br/>




