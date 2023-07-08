

- **COURSE INFORMATION: CSN 400 NBB**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER ID: 0245861155-myseneca**
- **TEACHER’S NAME: Atoosa Nasiri**
<br>

1. [Part A - Creating & Configuring VMs - Using Azure CLI Scripts](#part-a)
2. [Part B - Basic Connectivity - Linux VMs Firewall Setting](#part-b)
3. [Part C - Azure Cost Analysis Charts](#part-c)




## Part A
#### answer for nic quesion
#### The nic delete is not on by default 
<br>

#### VM list
```
Name    ResourceGroup      Location       Zones
------  -----------------  -------------  -------
LR-61   STUDENT-RG-964259  canadacentral  1
LS-61   STUDENT-RG-964259  canadacentral  1
WC-61   STUDENT-RG-964259  canadacentral  1
WS-61   STUDENT-RG-964259  canadacentral  1
```
<br>

#### Disk list
```

Name                                             ResourceGroup      Location       Zones    Sku           OsType    SizeGb    ProvisioningState
-----------------------------------------------  -----------------  -------------  -------  ------------  --------  --------  -------------------
LR-61_OsDisk_1_2d2bef52193a4390881060282b8b1d64  STUDENT-RG-964259  canadacentral  1        Standard_LRS  Linux     64        Succeeded
LS-61_OsDisk_1_61c5b37394d84e8c8ca70b79fdec19f9  STUDENT-RG-964259  canadacentral  1        Standard_LRS  Linux     64        Succeeded
WC-61_OsDisk_1_b63d13f16c2843628e0c647c659756f1  STUDENT-RG-964259  canadacentral  1        Standard_LRS  Windows   127       Succeeded
WS-61_OsDisk_1_3e6389d899134f5d958d6938cf63020e  STUDENT-RG-964259  canadacentral  1        Standard_LRS  Windows   127       Succeeded
```
<br>

#### NSG list
```
Location       Name        ProvisioningState    ResourceGroup      ResourceGuid
-------------  ----------  -------------------  -----------------  ------------------------------------
canadacentral  lr-61-nsg   Succeeded            Student-RG-964259  4a8b53d6-b894-4aa1-85b5-a24bd6dd4888
canadacentral  LR61nsg400  Succeeded            Student-RG-964259  ab07b41e-7b95-472d-b185-8d0acedb94a5
canadacentral  ls-61-nsg   Succeeded            Student-RG-964259  d24cfbd1-cd94-4d59-9f1f-837ba828c64b
canadacentral  LS61nsg373  Succeeded            Student-RG-964259  960e48ff-6846-433e-81d0-cdcaa8768662
canadacentral  ls61nsg953  Succeeded            Student-RG-964259  a1190998-433f-4420-b26e-b2751bf7ed8c
canadacentral  WC-61-nsg   Succeeded            Student-RG-964259  9dbb79a8-bc2d-49c3-a5fb-c58ba29f5c20
canadacentral  WS-61-nsg   Succeeded            Student-RG-964259  4a99533b-f94f-4710-b776-086dc23c231d
```
<br>

#### nic list
```
EnableAcceleratedNetworking    EnableIPForwarding    Location       MacAddress         Name         NicType    Primary    ProvisioningState    ResourceGroup      ResourceGuid                          VnetEncryptionSupported
-----------------------------  --------------------  -------------  -----------------  -----------  ---------  ---------  -------------------  -----------------  ------------------------------------  -------------------------
False                          False                 canadacentral  00-0D-3A-F3-D5-8D  lr-61578_z1  Standard   True       Succeeded            Student-RG-964259  cbebd5b8-d609-402f-8bbc-d7a9bccc5080  False
False                          False                 canadacentral  00-22-48-AF-98-56  ls-61314_z1  Standard   True       Succeeded            Student-RG-964259  e1081c52-bb67-4f74-9f4e-20b310625ed5  False
False                          False                 canadacentral  00-0D-3A-0C-67-87  wc-6161_z1   Standard   True       Succeeded            Student-RG-964259  ceb3eaae-7584-4a0b-9854-d1a028e22b91  False
False                          False                 canadacentral  00-0D-3A-84-65-F5  ws-6183_z1   Standard   True       Succeeded            Student-RG-964259  92552060-5e00-481d-9a2d-26b618828d53  False

```

## Part B

## Part C
<img src="./images/azure cost.png" alt="azure dashboard" style="float: left; margin-right: 5px;" /> 