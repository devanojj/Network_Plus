### Step 1: Write out the networks

- 192.168.16.0/24
- 192.168.17.0/24
- 192.168.18.0/24
- 192.168.19.0/24

These are **4 contiguous /24 networks**.

### Step 2: Determine the new prefix

Every time you combine:

- 2 × /24 = **/23**
- 4 × /24 = **/22**
- 8 × /24 = **/21**

Since there are **4 networks**, the summary should be a **/22**.

### Step 3: Check the boundary

A **/22** network increments by **4** in the third octet:

- 192.168.0.0/22
- 192.168.4.0/22
- 192.168.8.0/22
- 192.168.12.0/22
- **192.168.16.0/22** ✅
- 192.168.20.0/22

The range of **192.168.16.0/22** is:

- 192.168.16.0 – 192.168.19.255

This exactly covers:

- ✅ 192.168.16.0/24
- ✅ 192.168.17.0/24
- ✅ 192.168.18.0/24
- ✅ 192.168.19.0/24

### Final Answer

**192.168.16.0/22** ✅