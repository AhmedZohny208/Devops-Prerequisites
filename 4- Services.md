# Services

Once you install a software on servers especially those that run in the background such as web servers or database servers, you would need to make sure that those servers or services are running even after the servers are rebooted

So services in linux help you configure software to run in the background and make sure that they run all the time automatically when servers are rebooted as well as they follow the right order of startup

When any software runs as a service in the background is installed, they are automatically configured as service on the system

### To start service [Start HTTPD service]
```bash
service httpd start
```

### The newer method to start a service
```bash
systemctl start httpd
```
So in this case system cuddle or system ctl start httpd

##### Systemctl:
Used to manage services on a systemd managed server

The service command uses Systemctl utility underneath, so we will focus on systemctl

### To stop service [Stop HTTPD service]
```bash
systemctl stop httpd
```

### Check HTTPD service Status
```bash
systemctl status httpd
```

### To configure a service to start automatically when the system boots up
```bash
systemctl enable httpd
```

### To disable the service at boots up
```bash
systemctl disable httpd
```

---

## How do you configure a program or software as a service?

For example, you have a simple python program

To run dev server
```bash
/usr/bin/python3 /opt/code/my_app.py
```

Once it's running, call localhost
```bash
curl http://localhost:5000
```

#### I want to configure this as a service

The systemctl command is used to manage the systemd services so we must configure our program as a systemd service

A systemd service is configured using a systemd unit file. These files may be located at **/etc/systemd/system**

**So let's create a unit file at this path**

<span style="background-color: green; color: white; padding: 4px 8px">my_app.service</span>
```bash
[service]
ExecStart=/usr/bin/python3 /opt/code/my_app.py
```

```bash
systemctl daemon-reload
systemctl start my_app
systemctl status my_app
curl http://localhost:5000
systemctl stop my_app
```

##### Notes
1. Define a section >> [service] and provide a directive named "ExecStart" = command that runs the application. That's enough to configure your application as a service.
2. **systemctl daemon-reload:** To let systemd know that there is a new service configured 

---

## How do you configure a service to automatically run when the system boots up?

<span style="background-color: green; color: white; padding: 4px 8px">my_app.service</span>
```bash
[Unit]
Description=My python web application

[service]
ExecStart=/usr/bin/python3 /opt/code/my_app.py
ExecStartPre=/opt/code/configure_db.sh
ExecStartPost=/opt/code/email_status.sh
Restart=always

[Install]
wantedBy= multi-user.target
```

##### Notes
1. **[Install]:** in this section, we need to configure this service to run after a particular service that runs at boot up. So one way to specify that is using the wantedBy directive. 

This line means that this service will run after multi-user.target is started 

Once this is done, you can configure the service to start during boot up using 

```bash
systemctl enable my_app
```

2. "ExecStartPre" and "ExecStartPost": If the app has other dependencies such as comands and scripts to be run before or after starting the app

3. If you'd like the app to automatically restart in case it crashes