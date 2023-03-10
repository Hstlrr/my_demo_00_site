---
title: "blameless-postmortem"
date: 2023-02-20T19:23:42Z
draft: true
---

# Parts Unlimited

## Phoenix Project - post mortem (incident #1738)

**Date**: 09-12-1997

**Authors**: Bushey

**Summary**: 
- The Phoenix EPOS system leaked billing information- double charged customers.- the POS instore was down.- Lost track of order information
  
 **Impact**:
- Loss of revenue, customer trust
- Estimated financial impact is still being assessed 
- Storing credit card CVV2 information in violation of payment industry rules - potential fines
  
- **root causes**
- Management was dismissive of technical IT and development concerns   
- poor communication between teams- Inadequate virtualisation planning and execution
 - Poor database maintenance tools  
- Slow database conversion- Lack of physical storage space with onsite servers
  
- **Trigger**:
- inadequate testing and validation of the management system- database conversion not completed before store opening
  
  # Timeline    

  ## Friday
 - **16:00** IT Operations team was assembled in preparation for the deployment at 4 p.m. But there was nothing to do because we hadn’t received anything from Chris’ team
 - **16:30** William the developer was upset that no one could get all of the Phoenix code to run in the test environment and were failing critical tests. Chris had to call them back in, and William’s team had to wait for the developers to send them new versions
  - **17:30** The Phoenix project was scheduled to start
  -  **19:30** Chris’s team still making changes. Phoenix was not available in the test environment and was still failing critical tests.
   - **21:00** wes discovers the phoenix database conversion was thousands of times slower than  expected and was still only 10% complete