# Bug Bounty Checklist for Web Application

> Personal workflow for authorized security testing and bug bounty programs ;)  
Happy hunting !  

## Table of Contents

* [Scope & Rule](#"Scope--Rule")
* [Recon & Assets Discovery](#Recon--Assets-Discovery)
* [Endpoint Enumeration](#Endpoint-Enumeration)
* [Information Gathering](#Information)
* [Authentication Review](#Authentication)
* [Session Review](#Session)
* [Authorization Review](#Authorization)
* [Input & Validation Review](#input--Validation-Review)
* [Business Logic Review](#Business)
* [Upload & API ](#API)
* [Client Side Review](#Client-Side-Review)
* [Reporting & Notes](#Reporting)


## <a name="Scope_&_Rule">Scope & Rule</a>  

- [ ] Read program rules 
- [ ] Verify in-scope assets
- [ ] Note exclusion
- [ ] Create working notes 


## <a name="Recon & Assets Discovery">Recon & Assets Discovery</a>  

### Asset Collection  

- [ ] Collect Subdomain   
- [ ] Collect historical URLs   
- [ ] Review public assets
- [ ] Review JavaScript files
- [ ] Identify technologies   

### Recon Validation 

- [ ] confirm reachable host   
- [ ] identify entry points  
- [ ] Map application structure 

### robots.txt Review

- [ ]  Check robots.txt for expose paths
- [ ]  Record referenced directories
- [ ]  Compare with discovering routes are publicly reachable

### Public Discovery Sources
- [ ]  Review archives and historical references
- [ ]  Review client-side references for undocumented routes
- [ ]  Identify publicly exposed hidden endpoints

### <a name="Endpoint Enumeration">Endpoint Enumeration</a>
- [ ]  Identify URL parameters
- [ ]  Identify API endpoints
- [ ]  Review headers
- [ ]  Review cookies
- [ ]  Track request flows
   
### <a name="Information Gathering">Information Gathering</a>

- [ ]  Manually explore the site
- [ ]  Identify Debug parameters 
- [ ]  Identify third-party hosted content
- [ ]  Identify all hostnames and ports
- [ ]  Identify co-hosted and related applications
- [ ]  Identify multiple versions/channels (e.g. web, mobile web, mobile app, web services)
- [ ]  Identify client-side code
- [ ]  Identify application entry points
- [ ]  Identify technologies used
- [ ]  Identify user roles
- [ ]  Perform Web Application Fingerprinting
- [ ]  Check for differences in content based on User Agent (eg, Mobile sites, access as a Search engine Crawler)
- [ ]  Check the caches of major search engines for publicly accessible sites
- [ ]  Check for files that expose content, such as robots.txt, sitemap.xml, .DS_Store
- [ ]  Spider/crawl for missed or hidden content

### <a name="Authentication Review">Authentication Review</a>

- [ ] Test for user enumeration
- [ ] Test for authentication bypass
- [ ] Test for brute force protection
- [ ] Test password quality rules
- [ ] Test remember me functionality
- [ ] Test for autocomplete on password forms/input
- [ ] Test password reset and/or recovery
- [ ] Test password change process
- [ ] Test CAPTCHA
- [ ] Test multi factor authentication
- [ ] Test for logout functionality presence
- [ ] Test for cache management on HTTP (eg Pragma, Expires, Max-age)
- [ ] Test for default logins
- [ ] Test for user-accessible authentication history
- [ ] Test for put-off channel notification of account lockouts and successful password changes

  
### <a name="Session Review">Session Review</a>

- [ ] Establish how session management is handled in the application (eg, tokens in cookies, token in URL)
- [ ] Check session tokens for cookie flags (http Only and secure)
- [ ] Check session cookie scope (path and domain)
- [ ] Check session cookie duration (expires and max-age)
- [ ] Check session termination after a maximum lifetime
- [ ] Check session termination after relative timeout
- [ ] Check session termination after logout
- [ ] Test to see if users can have multiple simultaneous sessions
- [ ] Test session cookies for randomness
- [ ] Confirm that new session tokens are issued on login, role change and logout
- [ ] Test for consistent session management across applications with shared session management
- [ ] Test for session puzzling
- [ ] Test for CSRF and clickjacking


### <a name="Authorization Review">Authorization Review</a>


- [ ]  Test for missing authorization
- [ ]  Test for horizontal Access control problems (between two users at the same privilege level)
- [ ]  Test for vertical Access control problems (a.k.a. Privilege Escalation)
- [ ]  Test for bypassing authorization schema
- [ ]  Test for path traversal

### <a name="Input & Validation Review">Input & Validation Review  </a>


- [ ]  Input handling  
- [ ]  Redirect handling  
- [ ]  Error handling  
- [ ]  API validation   


### <a name="Business Logic Review">Business Logic Review</a>

- [ ]  Test for Workflow validation
- [ ]  Test for Abuse scenarios
- [ ]  Rate limits
- [ ]  Integrity check 

### <a name="API Review">Upload & API Review </a>
- [ ]  Test for File restriction   
- [ ]  Test for Upload controls 
- [ ]  Test for API consistency
- [ ]  Test for Response comparison
 
### <a name="Client Side Review">Client Side Review</a>

- [ ]  JavaScript review  
- [ ]  Source map
- [ ]  Exposed references


### <a name="HTML">HTML 5</a>
- [ ]  Test Web Messaging  
- [ ]  Test for Web Storage SQL injection  
- [ ]  Check CORS implementation  
- [ ]  Check Offline Web Application  


### <a name="Reporting">Reporting & Notes</a>
- [ ]  Reproduce 
- [ ]  Evidence
- [ ]  Impact
- [ ]  Exposed references 

Personal methodology
 
Inspired by [OWASP](https://www.owasp.org/index.php/Web_Application_Security_Testing_Cheat_Sheet) 
