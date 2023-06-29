



- **COURSE INFORMATION: CSN 400 NBB**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER ID: 0245861155-myseneca**
- **TEACHER’S NAME: Atoosa Nasiri**
<br>

## Part A

### Answer
#### The difference between Windows machine NSG and Linux machine NSG rules lies in the protocols and ports used by each operating system. Windows typically uses RDP (port 3389), while Linux uses SSH (port 22). Deleting specific SSH or RDP rules would block remote access using those protocols.



```
odl_user [ ~ ]$ az vm list --output table
Name    ResourceGroup      Location       Zones
------  -----------------  -------------  -------
LR-61   STUDENT-RG-964259  canadacentral  1
LS-61   STUDENT-RG-964259  canadacentral  1
WC-61   STUDENT-RG-964259  canadacentral  1
WS-61   STUDENT-RG-964259  canadacentral  1

```

## Part B

```json
odl_user [ ~ ]$ az network nic show -g Student-RG-964259 -n lr-61525_z1 --query "enableipforwarding" 
odl_user [ ~ ]$ 
```

## Part C