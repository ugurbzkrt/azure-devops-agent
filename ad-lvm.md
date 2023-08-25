## Azure DevOps Linux Agent:

$ https://vstsagentpackage.azureedge.net/agent/2.213.2/vsts-agent-linux-x64-2.213.2.tar.gz

$ mkdir myagent && cd myagent
~/myagent$ tar zxvf ~/Downloads/vsts-agent-linux-x64-2.213.2.tar.gz

~/myagent$ ./config.sh

  - Enter server info. and cred.
  - PAT = Token.

  - Negotiate = username-passwd.

Fail:
```
GSSAPI operation failed with error - An unsupported mechanism was requested. NTLM authentication requires the GSSAPI plugin 'gss-ntlmssp'.
Failed to connect.  Try again or ctrl-c to quit
```
Solution:

$ apt update -y
$ sudo apt install gss-ntlmssp -y


$ ./run.sh

