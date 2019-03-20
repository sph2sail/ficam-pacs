---
layout: default
title: Aligning Facility Security Level (FSL) and Authentication
permalink: /alignfslandauth/
---

Federal agencies rely on PACS and PIV credentials to confirm that an employee, contractor, or visitor _is_ or _is not_ authorized to access a site and its critical assets (systems, information, people, etc.). 

To ensure that your agency's critical assets are protected, you will need to assess each site's risk level (called *Facility Security Level*) and decide what level of PIV-credential authentication is required (called *authentication mechanism*). 

For agencies planning to procure an E-PACS, the FSL and Authentication checklist below will help you:

- Assess Facility Security Level (FSL)
- Categorize security areas
- Determine authentication factors
- Select the authentication mechanisms needed to protect critical assets

{% include alert-info.html content="These federal standards give the guidance for assessing FSL, including how to categorize site risks:<br> - <a href=\"https://www.dhs.gov/publication/isc-risk-management-process\" target=\"_blank\">The Risk Management Process for Federal Facilities: An Interagency Security Committee Standard </a> <br> - <a href=\"https://csrc.nist.gov/publications/detail/sp/800-116/rev-1/final\" target=\"_blank\">NIST SP 800-116, Revision 1, Guidelines for the Use of PIV Credentials in Facility Access. </a>" %}

<br>

<i class="fa fa-check-square-o"></i> &nbsp;**1. Assess Facility Security Level (FSL)**

- Inventory critical assets for each agency site.
    - When you inventory critical assets, also document any challenges to securing them.  <br><br>Examples of critical assets are:
        - Information systems and IT infrastructure
        - People
        - Campus, building, secure vaults, armory, etc.
        - Tenant agencies' information systems, IT infrastructure, and people
  
    - If you must evaluate an asset's criticality, consider:
        - Security classification level
        - The impact on national security from potential asset loss, compromise, or damage
        - Cost of replacing the asset

- Assess site and critical asset risks, as well as risks to tenant agencies' assets.
    - Examples of potential risks to a site and its critical assets are: 
        - Site mission(s) (i.e., those of the agency, its organizations, and tenant agencies)
        - Site “symbolism” (i.e., public perception of the agency, its organizations, tenant agencies, or missions)
        - Total population (i.e., employees plus contractors)
        - Size (square footage) 
        - Geographical location
        - Proximity to other facilities or structures not owned by the agency
        - Threats specific to tenant agencies 
        
    - Consider the following for each asset: 
        - Criticality - Is it mission-critical?
        - Sensitivity - Does it contain classified or sensitive information?
        - Likelihood - Probability of loss, compromise, or damage

- Categorize each asset by risk impact level. [FIPS 199](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.199.pdf){:target="_blank"} defines 3 impact levels on organizations and people (i.e., a loss of confidentiality, integrity, or availability): *Low*, *Moderate*, and *High*.  

- Create a site map of categorized assets.
> **Note:** This map will help you to determine each security area's minimum security level.


{% include alert-info.html content="An alternative to assessing a site's risk is to select a pre-determined FSL, as described in <a href=\"https://www.dhs.gov/publication/isc-risk-management-process/\" target=\"_blank\">The Risk Management Process for Federal Facilities: An Interagency Security Committee Standard</a>." %}

<br>
<i class="fa fa-check-square-o"></i> &nbsp;**2.	Categorize security areas** 

Once you've inventoried and mapped assets by risk and impact levels, it's time to categorize security areas.

{% include alert-info.html content="Agencies may use different terms for their security areas; however, each agency should establish its criteria for authentication mechanisms, according to <a href=\"https://csrc.nist.gov/publications/detail/sp/800-116/rev-1/final/\" target=\"_blank\">NIST SP 800-116, Revision 1, Guidelines for the Use of PIV Credentials in Facility Access</a>." %}

NIST SP 800-116, Revision 1, defines three security area categories: <br>

|Category | Description|
|:---------|:------------|
| *Exclusion*| An area where uncontrolled movement would permit direct access to a security asset.|
| *Limited* | An area near a secure asset.  Uncontrolled movement within a limited area may permit access to an asset.  Escorts and other restrictions can prevent access.| 
|*Controlled* | An area near or surrounding a Limited or Exclusion area. A Controlled area provides administrative control, safety, or a buffer zone for embedded Limited or Exclusion areas.  Movement of authorized personnel within this area is normally not controlled, as this area doesn't provide immediate access to secure assets.  |

- Assign the same risk level as the highest risk asset within the area. <br><br> 
Example: If 3 assets exist within a security area: one Low-risk, one Moderate-risk, and one High-risk, you must categorize the security area as **High-risk**.  Alternatively, the area may be split into 3 security areas that each have a different risk level.  

> **Note:** Each agency should determine the security measures required to protect their assets.  For example, an agency may categorize a security area with High-risk assets as a Limited security area and accept the associated risks.

<br>
<i class="fa fa-check-square-o"></i> &nbsp;**3.	Determine authentication factors** 

- Once you have categorized all security area categories, you will select the minimum number of authentication factors (1, 2, or 3) needed to access (and safeguard) the facility.

| Category| Minimum Number of Factors | Description|
|:---------|:--------------------------:|:------------|
|*Exclusion*| 3| Exclusion areas require the authentication factors:  Something you have (e.g., a PIV), Something you know (e.g., a PIN), and Something you are (e.g., a fingerprint or iris scan).|
|*Limited* | 2 | Limited areas require 2 of the 3 authentication factors:  a PIV and PIN, a PIV and fingerprint or iris scan, or a PIN and fingerprint or iris scan.|
|*Controlled* | 1 | Controlled areas require only one authentication factor:  a PIV, a PIN, or a fingerprint/iris scan. (There are currently no FICAM-approved, one-factor biometric readers.)|  
  
<br>
<i class="fa fa-check-square-o"></i> &nbsp;**4. Select authentication mechanism** 

- Based on the security area categories and required authentication factors required for each security area, choose the PIV-credential authentication mechanism(s) that enforce these factors at each access point. 

{% include alert-info.html content="FIPS 201-2 defines authentication mechanisms at four assurance levels (Little or No, Some, High, and Very High)." %}

FIPS 201-2 specifies these authentication mechanisms for PIV credentials:

- PKI authentication using the PIV Authentication Certificate (PKI-AUTH)
- PKI authentication using the Card Authentication Certificate (PKI-CAK)
- Authentication using the Symmetric Card Authentication Key (SYM-CAK)
- Unattended authentication using off-card biometric comparisons (BIO)
- Attended authentication using off-card biometric comparisons (BIO-A)
- Either attended or unattended authentication using off-card biometric comparisons (BIO(-A))
- Authentication using on-card biometric comparisons (OCC-AUTH)

The table below gives the possible authentication mechanisms for the 3 security area categories.

| Category  | Minimum<br>Number of<br>Factors | Acceptable Factors | Authentication<br>Mechanism:<br>Contact Interface  |  Authentication Mechanism:<br>Contactless Interface |
| :-------- | :------: | :----- | :-----  | :-----     |
| *Controlled*   | 1 | Something you have **OR**<br>Something you are  |  PKI-CAK  | PKI-CAK<br> SYM-CAK   |
| *Limited*   | 2 |Something you have *AND*<br>Something you know, **OR**<br>Something you have *AND*<br>Something you are, **OR**<br>Something you know *AND*<br>Something you are  | PKI-AUTH (with PIN or OCC) or<br>OCC-AUTH  |  OCC-AUTH |
| *Exclusion*  | 3 | Something you have **AND**<br>Something you know **AND**<br>Something you are | PKI-CAK + BIO(-A)  | N/A |

> **Note:** When using PKI-CAK and PKI-AUTH as authentication mechanisms, certificates must be validated. Verify the certificate against a Certificate Revocation List (CRL) or Online Certificate Status Protocol (OCSP) server response. Also, verify that the certificate chains to the Federal Common Policy root certification authority (CA).

The next section, *[Procurements]({{site.baseurl}}/procure/)*, describes the processes and resources needed for an E-PACS procurement.

