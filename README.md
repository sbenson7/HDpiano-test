# HDpiano Test

**1. Briefly, how/where did you start your WordPress development career.**

I started using Wordpress as a junior in college, interning for the creative agency [Idea Kraft](https://idea-kraft.com/), where I worked on WordPress sites for clients.

**2. What code editor are you using?**

Sublime Text

**3. What are your favorite paid WordPress plugins?**

WP Rocket, Akismet, BackUp Buddy

**4. If freelancing, how much would you generally charge for hourly work?**

$50

**5. If you were to build a new website, how would you go about it? Alter an existing theme? Build a custom theme from scratch? Something else?**

It depends on the client. Usually though, I'll just alter an existing theme if there is no need to reinvent the wheel.

**6. Describe the process of Php code debugging in WordPress.**

Open the wp-config.php file and add define('WP_DEBUG', true);. Save and close the file. Run the code that needs debugging and use the debugger output to locate and solve the problem. Once done, go to the same line of code and change true to false.

**7. How would you deploy any code changes to the production server?**

I'd use DeployBot for automated deployment by linking it to the GitHub repo where the code is stored, compiling dependencies via composer, adding any additional configuration files and then deploying.

**8. You need to make a change to a custom theme and you have the FTP. Describe how you would make the change detailing on every step.**

Got to WebFTP. Select the style.css file from the list in WebFTP, and click on Edit. Make your changes and hit Save. I would then test the website to ensure the changes were processed successfully.

**9. What's the last command you use to send changes to Github?**

git push origin master

**10. What git client are you using?**

GitHub Desktop

**11. Correct the following snippet that depends on jQuery.**

``` php
add_custom_script();
    function add_custom_script(){
        wp_enqueue_script( 
            'jquery-custom-script',
            get_template_directory_uri.'js/jquery-custom-script.js',
            array('jquery'),
            false,
            false
        );
    }
```
**12. The code below produces the following error `$ is not defined` in WordPress, Jquery is present in the header and we are using a default WordPress theme with no plugins. How would you fix it?**

``` javascript
    jQuery(document).ready(function($){
        $("ul.vimeo_desc_feed li a").click(function(){
          console.log('test');
        })
    });
```

**13. Please change the code below to make this database query the WordPress way, and to also secure it against SQL injection.**

``` php
function perform_database_action(){
    $value1 = $_GET['param1'];
    $value2 = $_GET['param2'];
    $value3 = $_GET['param3'];
    $wpdb->prepare( "INSERT into table_name (col1, col2, col3) VALUES ('%s', '%s', '%s')", array($value1, $value2, $value3) );
}
```
**14. Explain what the following CSS selectors will do:**
``` scss
div, p /* the CSS is applied to all div elements and all p elements */
div p /* the CSS is applied to all p elements within div elements  */
div > p /* the CSS is applied to all p elements where the parent is div  */
div + p /* the CSS is applied to the first p element directly below div elements  */
div ~ p /* the CSS is applied to all p elements below all div elements that share a parent */

a:hover /* the CSS is applied when the cursor is hovering over a link element   */
div p:first-child /* the CSS is applied to the first element within each p element inside a div element */
div p:nth-child(n) /* the CSS is applied to the nth element within each p element inside a div element*/
#amazing-div::before /* the CSS is applied to content before the content of #amazing-div */
```

**Bonus: How would you select every second child element?**


**15. In CSS3, how would you select:**

_- Every `<a>` element whose href attribute value begins with “https”._ 
a[href^="https"]

_- Select every `<a>` element whose href attribute value ends with “.pdf”:_ 
a[href$=".pdf"]

_- Select every `<a>` element whose href attribute value contains the substring “css”:_ 
a[href*="css"]

**16. Can you tell us what is missing from this plugin to make it useable?**

Plugin Name: Name of the Plugin

**17. What color would be the anchor inside p?**

Red

**18. Get the parent with class `targetMe` starting from element with the class `startHere`**

```javascript
    jQuery(document).ready(function($){
        $('.startHere').closest('.targetMe');
    });
```
**19. How would you make each .item element appear in its own evenly spaced column using flexbox? (only 2 css rules needed)**

``` scss
.container {
  display: flex;
  align-items: center;
  justify-content: center;
}

.container .item {
  width: 100%;
  height: 100%;
}
```  

**20. Pre-Assignment Questions:**

**- Please estimate how long it will take you to deliver the plugin below.**

I'd estimate between 1-3 hours. 

**- If you were asked to take on the project below for a client, please estimate how much this would cost (this is the amount we will pay you if you make it through the preliminary review).**

$150

