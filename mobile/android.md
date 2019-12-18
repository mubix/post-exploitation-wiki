## Using meterpreter:
#### Meterpreter shell useful commands for android post-exploitation
| Commands        | Functionality                                                                                                                                                                                                                   |
|:--------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `webcam_chat`   | This module allows streaming a webcam from a privileged Firefox Javascript shell.                                                                                                                                               |
| `webcam_list`   | The ‘webcam_list‘ command when run from the Meterpreter shell, will display currently available web cams on the target host.                                                                                                    |
| `webcam_snap`   | The ‘webcam_snap’ command grabs a picture from a connected web cam on the target system, and saves it to disc as a JPEG image. By default, the save location is the local current working directory with a randomized filename. |
| `webcam_stream` | The webcam_stream command basically uses the webcam_snap command repeatedly to create the streaming effect. There is no sound.                                                                                                  |
| `dump_calllog`  | The dump_calllog command retrieves the call log from the Android device.                                                                                                                                                        |
| `dump_contacts` | The dump_contacts command allows you to retrieve contacts information form the android device.                                                                                                                                  |
| `dump_sms`      | The dump_sms command allows you to retrieve SMS messages. And save them as a text file.                                                                                                                                         |
| `geolocate`     | The geolocate commands allows you to locate the phone by retrieving the current lat-long using geolocation.                                                                                                                     |
| `check_root`    | The check_root command detects whether your payload is running as root or not.                                                                                                                                                  |
| `upload`        | The upload command allows you to upload a file to the remote target. The -r option allows you to do so recursively.                                                                                                             |
| `download`      | The download command allows you to download a file from the remote target. The -r option allows you to do so recursively.                                                                                                       |
| `shell`         | The shell command allows you to interact with a shell.                                                                                                                                                                          |
| `sysinfo`       | The sysinfo command shows you basic information about the Android device.                                                                                                                                                       |
| `record_mic`    | The record_mic command records audio. Good for listening to a phone conversation, as well as other uses.                                                                                                                        |
| `send_sms`      | The send_sms command allows you to send an SMS message. Keep in mind the phone will keep a copy of it, too.                                                                                                                                                                                                                                |

Other commands:


#### Way to change password of services.
You can recover password for some services (like gmail, twitter and facebook) by receiving SMS message.
First, click "forgot password" and select SMS options. Then use the command `dump_sms` and you will have
verification code. Insert the code and change the password.



## Other post-exploitation tools
#### Pupy:
Pupy is an opensource, cross-platform (Windows, Linux, OSX, Android), multi function RAT (Remote Administration Tool) and post-exploitation tool mainly written in python. It features a all-in-memory execution guideline and leaves very low footprint. Pupy can communicate using various transports, migrate into processes (reflective injection), load remote python code, python packages and python C-extensions from memory.

#### TheFatRat:
An easy tool to generate backdoor and easy tool to post exploitation attack like browser attack,dll . This tool compiles a malware with popular payload and then the compiled malware can be execute on windows, android, mac . The malware that created with this tool also have an ability to bypass most AV software protection.

#### Xenotix-APK-Reverser
Xenotix APK Reverser is an OpenSource Android Application Package (APK) decompiler and disassembler powered by dex2jar, baksmali and jd-core Released under Apache License.

#### DynamoRIO
DynamoRIO is a runtime code manipulation system that supports code transformations on any part of a program, while it executes. DynamoRIO exports an interface for building dynamic tools for a wide variety of uses: program analysis and understanding, profiling, instrumentation, optimization, translation, etc. Unlike many dynamic tool systems, DynamoRIO is not limited to insertion of callouts/trampolines and allows arbitrary modifications to application instructions via a powerful IA-32/AMD64/ARM/AArch64 instruction manipulation library. DynamoRIO provides efficient, transparent, and comprehensive manipulation of unmodified applications running on stock operating systems (Windows, Linux, or Android) and commodity IA-32, AMD64, ARM, and AArch64 hardware.

We can run DynamoRIO based plugin to detect any post exploitation privilege escalation. E.g., java.lang.Runtime.exec("su") is generally used for getting su privileges using setuid(0) system call. These functions is detected using a global call.


## Methodology
#### Steps
1. Application Mapping
In this first phase, the focus relies on understanding the application logic and what exactly the application does. This involves some manual test where we do some basic operations such as install the APK on the phone, login and comprehend the functionality of the app.

1. Client Attacks
This is one of the most challenging and exciting parts of the pentest assessment. Android apps are packed as an APK, also known as Android Package Kit or Android Application Package. Our mission as Pen testers is to verify how well protected the application has been created and designed against known threat actors.Android Mobile applications are distributed through platforms like Google Play. Since the application is fully installed on the client, it becomes vulnerable to any attacks coming from the client.

1. Network Attacks
As we need to identify vulnerabilities in the Client, is also essential to verify how secure is the communication between the Client and the Server by evaluating the traffic. For this purpose, using tools like Attack proxies, evaluating potential SSL issues, and executing Wireshark Data package inspection is an essential part of the assessment.

1. Server Attacks
Last but not least, issues at the Server level will impact the security of the application. Insecure implementation such as misconfigurations , vulnerabilities and issues at API or Database level, affect also the security of an application


# Refernce:
### android shell command:
- https://github.com/jackpal/Android-Terminal-Emulator/wiki/Android-Shell-Command-Reference
- https://docs.google.com/document/d/1XaCCyAf46_gQYUIWHyRSCQue6d-TzJmKOZ1z1cpl1sI/edit
- https://android.stackexchange.com/questions/11052/what-useful-android-shell-commands-do-you-know
- https://github.com/rapid7/metasploit-framework/blob/master/documentation/modules/payload/android/meterpreter/reverse_tcp.md
- https://null-byte.wonderhowto.com/how-to/hack-android-using-kali-remotely-0160161/
- http://ddosdipdye.weebly.com/blog/big-android-hacking-article
- http://www.hackingarticles.in/hack-call-logs-sms-camera-remote-android-phone-using-metasploit/
- https://android.stackexchange.com/questions/60906/terminal-on-real-android-device-from-pc
- https://github.com/n1nj4sec/pupy
- https://github.com/Screetsec/TheFatRat
- https://github.com/ajinabraham/Xenotix-APK-Reverser
- https://www.owasp.org/index.php/Android_Testing_Cheat_Sheet
- http://www.dynamorio.org
