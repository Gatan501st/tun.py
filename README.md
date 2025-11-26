# tun.py


Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.14.1-1.msi -OutFile $env:tmp\wazuh-agent; msiexec.exe /i $env:tmp\wazuh-agent /q WAZUH_MANAGER='ksy0ce7dascz.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD='FmN59ziA66OITDBgwvBB0U3C8yn1Nxl5' WAZUH_AGENT_NAME='windows1' 



wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.14.1-1_amd64.deb && sudo WAZUH_MANAGER='ksy0ce7dascz.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD=$'FmN59ziA66OITDBgwvBB0U3C8yn1Nxl5' WAZUH_AGENT_NAME='ubuntu3' dpkg -i ./wazuh-agent_4.14.1-1_amd64.deb

sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
