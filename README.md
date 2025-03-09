<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

-  PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
-  Rewrite Module (rewrite_amd64_en-US.msi)
-  VC_redist.x86.exe.
-  MySQL 5.5.62 (MySQL-5.5.62-win32.msi)
- Create the directory C:\PHP

<h2>Installation Steps</h2>

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420713270-6e0c5317-3a28-4bff-834f-9603a85d239e.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T232146Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=ec624c9da05b2e2aaecc1f0bd21f482d8381b7fb7117f2ed4097615a5234cfd0&amp;X-Amz-SignedHeaders=host">
</p>
<p>
Download and unzip the osTicket-Installation-Files.zip.
Then Install all the Prerequisites in the osTicket-Installation-Files.
</p>
<br />

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420713847-6d9a490f-0f55-41c4-a3ef-bd3a3d2934a2.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T232718Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=230ce37490de41c17986654c93554c334bc8e255f29198eb5136729edf3e31ec&amp;X-Amz-SignedHeaders=host">
</p>
<p>
Open IIS as an Admin
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420713979-f5ff7b57-5938-4d9f-a2c2-6472be22195c.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T232932Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=b63ec9fc7c39cf98d05e3b399d6419383e8451a09c999d726a87aeb5c37d3b61&amp;X-Amz-SignedHeaders=host">
</p>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
  
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

</p>
<br />

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420714383-902e6dbd-dfca-40ea-a3e9-69481cc42c80.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T233430Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=494c54708c1c0ff9f8d7aaa59ddfb0ab19fef8dd5d5117c98f8b22dd48413eb0&amp;X-Amz-SignedHeaders=host">
</p>
<p>

Rename: "ost-config.php" to "ost-config.php" in C:\inetpub\wwwroot\osTicket\include
Assign Permissions: ost-config.php
Disable inheritance -> Remove All

New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420714935-a3d237ca-01d0-4c5f-b29c-da0a684c5177.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T234156Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=8cccacdc65b97cff178fd818b4180417c602f5193e980da88e30003215a38ad6&amp;X-Amz-SignedHeaders=host" width="296" height="166">
</p>

From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420714241-35183654-bbab-44e7-9038-f1b1abd587a4.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T233222Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=8e6c9c852306f4f726c899f56a5f9958dfec9030ee5fbdeb235fb8af53dbe88b&amp;X-Amz-SignedHeaders=host">
</p>

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

<p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://github-production-user-asset-6210df.s3.amazonaws.com/142127371/420714587-f62aba2c-3861-4979-946c-b805b30bf938.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250309%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20250309T233738Z&amp;X-Amz-Expires=300&amp;X-Amz-Signature=ac8df53a1e397233a00fab691c6646416e6f9ce64bdacd78b45ee83d17bda37d&amp;X-Amz-SignedHeaders=host">
</p>

Congratulations, hopefully it is installed with no errors!
</p>
<br />
