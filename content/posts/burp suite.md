2024-06-05 18:27  
Status:
Tags: [[web security]] [[kali]] [[cyber security]] [[linux]] [[hacking]] [[CS]]
# LINKS



# NOTES
utulized as proxy

Burp Suite is a comprehensive platform for web application security testing. Developed by PortSwigger, it provides tools for performing security testing of web applications. It is widely used by security professionals, developers, and testers to identify and exploit vulnerabilities in web applications.

### Key Features of Burp Suite:

1. **Proxy**:
    
    - Acts as an intercepting proxy to capture and inspect HTTP/S traffic between the browser and the web server.
    - Allows for modification of requests and responses on the fly.
2. **Spider**:
    
    - Automatically crawls the web application to map out its structure and discover content and functionality.
3. **Scanner**:
    
    - Identifies vulnerabilities such as SQL injection, cross-site scripting (XSS), and other common web application flaws.
    - Available in the Professional edition with automated scanning capabilities.
4. **Intruder**:
    
    - Automates customized attacks against web applications, such as brute force attacks, fuzzing, and parameter manipulation.
    - Useful for testing the strength of passwords and the application's handling of unexpected input.
5. **Repeater**:
    
    - Allows for manual modification and re-sending of individual HTTP requests to test how the application responds to different inputs.
6. **Sequencer**:
    
    - Analyzes the randomness of tokens, such as session cookies, to identify weaknesses in session management.
7. **Decoder**:
    
    - Decodes and encodes data in various formats, such as URL encoding, Base64, and HTML encoding.
8. **Comparer**:
    
    - Compares two sets of data to identify differences, useful for identifying changes in application behavior.
9. **Extender**:
    
    - Allows for the extension of Burp Suite's functionality through the use of plugins and the Burp Extender API.
    - Supports community-developed extensions to enhance Burp Suite's capabilities.

### Editions of Burp Suite:

1. **Community Edition**:
    
    - Free version with limited features.
    - Suitable for basic manual testing and learning purposes.
2. **Professional Edition**:
    
    - Paid version with full functionality.
    - Includes advanced scanning, automated testing, and additional tools and features.
3. **Enterprise Edition**:
    
    - Designed for automated, scalable security testing in CI/CD environments.
    - Provides continuous scanning and integration with development pipelines.

### Use Cases for Burp Suite:

- **Penetration Testing**: Security professionals use Burp Suite to perform thorough security assessments of web applications.
- **Bug Bounty Hunting**: Researchers and ethical hackers use Burp Suite to find and report vulnerabilities in web applications.
- **Development and QA**: Developers and QA engineers use Burp Suite to identify and fix security issues during the development lifecycle.

Burp Suite is a powerful tool for web application security testing, offering a range of features that cater to both manual and automated testing needs.


# Tutorial
https://portswigger.net/burp/documentation/desktop/getting-started

## ntercepting a request

Burp Proxy lets you intercept HTTP requests and responses sent between Burp's browser and the target server. This enables you to study how the website behaves when you perform different actions.

### Step 1: Launch Burp's browser

Go to the **Proxy > Intercept** tab.

Click the **Intercept is off** button, so it toggles to **Intercept is on.**

![Intercept is on](https://portswigger.net/burp/documentation/desktop/images/getting-started/quick-start-pro-intercept-on.png)

Click **Open Browser**. This launches Burp's browser, which is preconfigured to work with Burp right out of the box.

Position the windows so that you can see both Burp and Burp's browser.

![Opening Burp's browser](https://portswigger.net/burp/documentation/desktop/images/getting-started/quick-start-pro-browser.png)

### Step 2: Intercept a request

Using Burp's browser, try to visit `https://portswigger.net` and observe that the site doesn't load. Burp Proxy has intercepted the HTTP request that was issued by the browser before it could reach the server. You can see this intercepted request on the **Proxy > Intercept** tab.

![Viewing an intercepted request in Burp Proxy](https://portswigger.net/burp/documentation/desktop/images/getting-started/quick-start-pro-intercepted-request.png)

The request is held here so that you can study it, and even modify it, before forwarding it to the target server.

### Step 3: Forward the request

Click the **Forward** button several times to send the intercepted request, and any subsequent ones, until the page loads in Burp's browser.

### Step 4: Switch off interception

Due to the number of requests browsers typically send, you often won't want to intercept every single one of them. Click the **Intercept is on** button so that it now says **Intercept is off**.

![Proxy Intercept is off](https://portswigger.net/burp/documentation/desktop/images/getting-started/quick-start-pro-intercept-off.png)

Go back to the browser and confirm that you can now interact with the site as normal.

### Step 5: View the HTTP history

In Burp, go to the **Proxy > HTTP history** tab. Here, you can see the history of all HTTP traffic that has passed through Burp Proxy, even while interception was switched off.

Click on any entry in the history to view the raw HTTP request, along with the corresponding response from the server.

![Viewing the HTTP history in Burp Proxy](https://portswigger.net/burp/documentation/desktop/images/getting-started/quick-start-pro-proxy-history.png)

This lets you explore the website as normal and study the interactions between Burp's browser and the server afterward, which is more convenient in many cases.






