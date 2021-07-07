<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="">
<meta name="keywords" content=" ">
<title>Bebop ROS | Tonylee Project Showcase</title>
<link rel="stylesheet" href="css/syntax.css">

<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
<!--<link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">-->
<link rel="stylesheet" href="css/modern-business.css">
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
<link rel="stylesheet" href="css/customstyles.css">
<link rel="stylesheet" href="css/boxshadowproperties.css">
<!-- most color styles are extracted out to here -->
<link rel="stylesheet" href="css/theme-blue.css">

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-cookie/1.4.1/jquery.cookie.min.js"></script>
<script src="js/jquery.navgoco.min.js"></script>


<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>
<!-- Anchor.js -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/anchor-js/4.2.0/anchor.min.js"></script>
<script src="js/toc.js"></script>
<script src="js/customscripts.js"></script>

<link rel="shortcut icon" href="images/favicon.ico">

<!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
<!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
<!--[if lt IE 9]>
<script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
<script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>
<![endif]-->

<link rel="alternate" type="application/rss+xml" title="documentation-theme-jekyll" href="http://localhost:4000/feed.xml">



    <script>
        $(document).ready(function() {
            // Initialize navgoco with default options
            $("#mysidebar").navgoco({
                caretHtml: '',
                accordion: true,
                openClass: 'active', // open
                save: false, // leave false or nav highlighting doesn't work right
                cookie: {
                    name: 'navgoco',
                    expires: false,
                    path: '/'
                },
                slide: {
                    duration: 400,
                    easing: 'swing'
                }
            });

            $("#collapseAll").click(function(e) {
                e.preventDefault();
                $("#mysidebar").navgoco('toggle', false);
            });

            $("#expandAll").click(function(e) {
                e.preventDefault();
                $("#mysidebar").navgoco('toggle', true);
            });

        });

    </script>
    <script>
        $(function () {
            $('[data-toggle="tooltip"]').tooltip()
        })
    </script>
    <script>
        $(document).ready(function() {
            $("#tg-sb-link").click(function() {
                $("#tg-sb-sidebar").toggle();
                $("#tg-sb-content").toggleClass('col-md-9');
                $("#tg-sb-content").toggleClass('col-md-12');
                $("#tg-sb-icon").toggleClass('fa-toggle-on');
                $("#tg-sb-icon").toggleClass('fa-toggle-off');
            });
        });
    </script>
    

</head>
<body>
<!-- Navigation -->
<nav class="navbar navbar-inverse navbar-static-top">
    <div class="container topnavlinks">
        <div class="navbar-header">
            <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
            </button>
            <a class="fa fa-home fa-lg navbar-brand" href="index.html">&nbsp;<span class="projectTitle"> Tonylee Project Documentation</span></a>
        </div>
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav navbar-right">
                <!-- toggle sidebar button -->
                <li><a id="tg-sb-link" href="#"><i id="tg-sb-icon" class="fa fa-toggle-on"></i> Nav</a></li>
                <!-- entries without drop-downs appear here -->




                
                
                
                <li><a href="https://github.com/aiegoo/portfolio/wiki" target="_blank" rel="noopener">GitHub</a></li>
                
                
                
                <li><a href="news">News</a></li>
                
                
                
                <!-- entries with drop-downs appear here -->
                <!-- conditional logic to control which topnav appears for the audience defined in the configuration file.-->
                
                
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown">Xaas<b class="caret"></b></a>
                    <ul class="dropdown-menu">
                        
                        
                        <li><a href="http://159.65.8.38:10024/en" target="_blank" rel="noopener">o-lora</a></li>
                        
                        
                        
                        <li><a href="http://159.65.8.38:10024/admin" target="_blank" rel="noopener">o-lora/admin aiegoo/</a></li>
                        
                        
                        
                        <li><a href="http://159.65.8.38:10024/blog" target="_blank" rel="noopener">o-lora/blog</a></li>
                        
                        
                        
                        <li><a href="http://idratherbewriting.com/category-jekyll/" target="_blank" rel="noopener">Jekyll on my blog</a></li>
                        
                        
                    </ul>
                </li>
                
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown">Xaas 2<b class="caret"></b></a>
                    <ul class="dropdown-menu">
                        
                        
                        <li><a href="mydoc_introduction.html">Conference call</a></li>
                        
                        
                        
                        <li><a href="p1_landing_page.html">LasVegas CES</a></li>
                        
                        
                        
                        <li><a href="p2_landing_page.html">Autonomous drone</a></li>
                        
                        
                    </ul>
                </li>
                
                
                
			<li>



  <a class="email" title="Submit feedback" href="#" onclick="javascript:window.location='mailto:onofftony@gmail.com?subject=Jekyll documentation theme feedback&body=I have some feedback about the Bebop ROS page: ' + window.location.href;"><i class="fa fa-envelope-o"></i> Feedback</a>

</li>



		
                <!--comment out this block if you want to hide search-->
                <li>
                    <!--start search-->
                    <div id="search-demo-container">
                        <input type="text" id="search-input" placeholder="search...">
                        <ul id="results-container"></ul>
                    </div>
                    <script src="js/jekyll-search.js" type="text/javascript"></script>
                    <script type="text/javascript">
                            SimpleJekyllSearch.init({
                                searchInput: document.getElementById('search-input'),
                                resultsContainer: document.getElementById('results-container'),
                                dataSource: 'search.json',
                                searchResultTemplate: '<li><a href="{url}" title="Bebop ROS">{title}</a></li>',
                    noResultsText: 'No results found.',
                            limit: 10,
                            fuzzy: true,
                    })
                    </script>
                    <!--end search-->
                </li>
            </ul>
        </div>
        </div>
        <!-- /.container -->
</nav>



<!-- Page Content -->
<div class="container">
  <div id="main">
    <!-- Content Row -->
    <div class="row">
        
        
            <!-- Sidebar Column -->
            <div class="col-md-3" id="tg-sb-sidebar">
                

<ul id="mysidebar" class="nav">
  <li class="sidebarTitle">my portfolio 1.0</li>
  
  
  
      
  
  <li>
      <a title="Overview" href="#">Overview</a>
      <ul>
          
          
          
          <li><a title="Get started" href="index.html">Get started</a></li>
          
          
          
          
          
          
          <li><a title="Introduction" href="mydoc_introduction.html">Introduction</a></li>
          
          
          
          
          
          
          <li><a title="Supported features" href="mydoc_supported_features.html">Supported features</a></li>
          
          
          
          
          
          
          <li><a title="About the theme author" href="mydoc_about.html">About the theme author</a></li>
          
          
          
          
          
          
          <li><a title="Support" href="mydoc_support.html">Support</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Automation" href="#">Automation</a>
      <ul>
          
          
          
          <li><a title="Ansible" href="mydoc_release_notes_60.html">Ansible</a></li>
          
          
          
          
          
          
          <li><a title="Git webhook" href="mydoc_release_notes_50.html">Git webhook</a></li>
          
          
          
          
          
          
          <li><a title="Bash pipeline" href="bash-pipeline.html">Bash pipeline</a></li>
          
          
          
          
          
          
          <li><a title="Docker" href="docker.html">Docker</a></li>
          
          
          
          
          
          
          <li><a title="Gitlab" href="gitlab.html">Gitlab</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="ROS, Serializer" href="#">ROS, Serializer</a>
      <ul>
          
          
          
          <li><a title="Rostopic integration" href="rostopic.html">Rostopic integration</a></li>
          
          
          
          
          
          
          <li><a title="Django restapi frameworks" href="djangorestapi.html">Django restapi frameworks</a></li>
          
          
          
          
          
          
          <li><a title="Gitlabithub actions" href="mydoc_install_jekyll_on_windows.html">Gitlabithub actions</a></li>
          
          
          
          
          
          
          <li><a title="pipeline, heroku, mailchimps" href="heroku.html">pipeline, heroku, mailchimps</a></li>
          
          
          
          
          
          
          <li><a title="others" href="others.html">others</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Django frameworks" href="#">Django frameworks</a>
      <ul>
          
          
          
          <li><a title="Oscar" href="oscar.html">Oscar</a></li>
          
          
          
          
          
          
          <li><a title="Raspi" href="raspi.html">Raspi</a></li>
          
          
          
          
          
          
          <li><a title="Lora" href="lora.html">Lora</a></li>
          
          
          
          
          
          
          <li><a title="Drone-gui" href="dronegui.html">Drone-gui</a></li>
          
          
          
          
          
          
          <li><a title="Content reuse" href="mydoc_content_reuse.html">Content reuse</a></li>
          
          
          
          
          
          
          <li><a title="Collections" href="mydoc_collections.html">Collections</a></li>
          
          
          
          
          
          
          <li><a title="WebStorm editor tips" href="mydoc_webstorm_text_editor.html">WebStorm editor tips</a></li>
          
          
          
          
          
          
          <li><a title="Atom editor tips" href="mydoc_atom_text_editor.html">Atom editor tips</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Node frameworks" href="#">Node frameworks</a>
      <ul>
          
          
          
          <li><a title="Django+Vue" href="djangovue.html">Django+Vue</a></li>
          
          
          
          
          
          
          <li><a title="Weather app" href="weather.html">Weather app</a></li>
          
          
          
          
          
          
          <li><a title="Chat app" href="chatapp.html">Chat app</a></li>
          
          
          
          
          
          
          <li><a title="Bootstrap" href="bootstrap.html">Bootstrap</a></li>
          
          
          
          
          
          
          <li><a title="lightup.co.kr/blog" href="lightup.html">lightup.co.kr/blog</a></li>
          
          
          
          
          
          
          <li><a title="lightup.co.kr/admin" href="lightupadmin.html">lightup.co.kr/admin</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Racing drones" href="#">Racing drones</a>
      <ul>
          
          
          
          <li><a title="DaLrC215" href="dalrc.html">DaLrC215</a></li>
          
          
          
          
          
          
          <li><a title="Dev-skyhero" href="skyhero.html">Dev-skyhero</a></li>
          
          
          
          
          
          
          <li><a title="MiniCp04" href="minicp.html">MiniCp04</a></li>
          
          
          
          
          
          
          <li><a title="Dev-Nazam 02" href="devnazam.html">Dev-Nazam 02</a></li>
          
          
          
          
          
          
          <li><a title="Xugong" href="xugong.html">Xugong</a></li>
          
          
          
          
          
          
          <li><a title="Labels" href="mydoc_labels.html">Labels</a></li>
          
          
          
          
          
          
          <li><a title="Links" href="mydoc_hyperlinks.html">Links</a></li>
          
          
          
          
          
          
          <li><a title="Navtabs" href="mydoc_navtabs.html">Navtabs</a></li>
          
          
          
          
          
          
          <li><a title="Tables" href="mydoc_tables.html">Tables</a></li>
          
          
          
          
          
          
          <li><a title="Syntax highlighting" href="mydoc_syntax_highlighting.html">Syntax highlighting</a></li>
          
          
          
          
          
          
          <li><a title="Workflow maps" href="mydoc_workflow_maps.html">Workflow maps</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="APM drones" href="#">APM drones</a>
      <ul>
          
          
          
          <li><a title="pixhawk4" href="mydoc_commenting_on_files.html">pixhawk4</a></li>
          
          
          
          
          
          
          <li><a title="Dev-Apmdr 01 / pixhawk lite" href="">Dev-Apmdr 01 / pixhawk lite</a></li>
          
          
          
          
          
          
          <li><a title="Cube black" href="">Cube black</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="DJI drones" href="#">DJI drones</a>
      <ul>
          
          
          
          <li><a title="Quad wookong" href="mydoc_build_arguments.html">Quad wookong</a></li>
          
          
          
          
          
          
          <li><a title="S1000 wookong" href="mydoc_themes.html">S1000 wookong</a></li>
          
          
          
          
          
          
          <li><a title="S1000 A2" href="mydoc_generating_pdfs.html">S1000 A2</a></li>
          
          
          
          
          
          
          <li><a title="S900 wookong" href="mydoc_help_api.html">S900 wookong</a></li>
          
          
          
          
          
          
          <li><a title="Nazam" href="mydoc_search_configuration.html">Nazam</a></li>
          
          
          
          
          
          
          <li><a title="iTerm profiles" href="mydoc_iterm_profiles.html">iTerm profiles</a></li>
          
          
          
          
          
          
          <li><a title="Pushing builds to server" href="mydoc_push_build_to_server.html">Pushing builds to server</a></li>
          
          
          
          
          
          
          <li><a title="Publishing on Github Pages" href="mydoc_publishing_github_pages.html">Publishing on Github Pages</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Feature drones" href="#">Feature drones</a>
      <ul>
          
          
          
          <li><a title="Yuneec H" href="mydoc_kb_layout.html">Yuneec H</a></li>
          
          
          
          
          
          
          <li class="active"><a title="Bebop Parrot" href="mydoc_bebop_auto.md">Bebop Parrot</a></li>
          
          
          
          
          
          
          <li><a title="Jetbot rover" href="mydoc_faq_layout.html">Jetbot rover</a></li>
          
          
          
          
          
          
          <li><a title="AGX Xavier rover" href="mydoc_shuffle.html">AGX Xavier rover</a></li>
          
          
          
          
          
          
          <li><a title="Vtol & flight data" href="">Vtol & flight data</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Schooling" href="#">Schooling</a>
      <ul>
          
          
          
          <li><a title="My courses" href="mydoc_troubleshooting.html">My courses</a></li>
          
          
          
          
          
          
          <li><a title="Course overview" href="">Course overview</a></li>
          
          
          
          
          
          
          <li><a title="Portfolio" href="">Portfolio</a></li>
          
          
          
          
          
          
          <li><a title="ncs-ML/DL" href="">ncs-ML/DL</a></li>
          
          
          
          
          
          
          <li><a title="C++" href="">C++</a></li>
          
          
          
          
          
          
          <li><a title="Web-scraping" href="">Web-scraping</a></li>
          
          
          
          
      </ul>
   </li>
     
      
  
  <li>
      <a title="Books" href="#">Books</a>
      <ul>
          
          
          
          <li><a title="Fiction" href="mydoc_tag_archives_overview.html">Fiction</a></li>
          
          
          
          <li class="subfolders">
              <a title="Tag archive pages" href="#">Tag archive pages</a>
              <ul>
                  
                  
                  
                  <li><a title="Formatting pages" href="tag_formatting.html">Formatting pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Navigation pages" href="tag_navigation.html">Navigation pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Content types pages" href="tag_content_types.html">Content types pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Publishing pages" href="tag_publishing.html">Publishing pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Special layout pages" href="tag_special_layouts.html">Special layout pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Collaboration pages" href="tag_collaboration.html">Collaboration pages</a></li>
                  
                  
                  
                  
                  
                  <li><a title="Troubleshooting pages" href="tag_troubleshooting.html">Troubleshooting pages</a></li>
                  
                  
                  
              </ul>
          </li>
          
          
          
          
          
          
          <li><a title="Web-dev-ops" href="">Web-dev-ops</a></li>
          
          
          
          
          
          
          <li><a title="" href=""></a></li>
          
          
          
          
          
          
          <li><a title="" href=""></a></li>
          
          
          
          
          
          
          <li><a title="" href=""></a></li>
          
          
          
          
          
          
          <li><a title="" href=""></a></li>
          
          
          
          
      </ul>
   </li>
     
      
      
      <!-- if you aren't using the accordion, uncomment this block:
         <p class="external">
             <a href="#" id="collapseAll">Collapse All</a> | <a href="#" id="expandAll">Expand All</a>
         </p>
         -->
</ul>

<!-- this highlights the active parent class in the navgoco sidebar. this is critical so that the parent expands when you're viewing a page. This must appear below the sidebar code above. Otherwise, if placed inside customscripts.js, the script runs before the sidebar code runs and the class never gets inserted.-->
<script>$("li.active").parents('li').toggleClass("active");</script>



            </div>
            
        

        <!-- Content Column -->
        <div class="col-md-9" id="tg-sb-content">
            <div class="post-header">
   <h1 class="post-title-main">Bebop ROS</h1>
</div>



<div class="post-content">

   

    
    
<!-- this handles the automatic toc. use ## for subheads to auto-generate the on-page minitoc. if you use html tags, you must supply an ID for the heading element in order for it to appear in the minitoc. -->
<script>
$( document ).ready(function() {
  // Handler for .ready() called.

$('#toc').toc({ minimumHeaders: 0, listType: 'ul', showSpeed: 0, headers: 'h2,h3,h4' });

/* this offset helps account for the space taken up by the floating toolbar. */
$('#toc').on('click', 'a', function() {
  var target = $(this.getAttribute('href'))
    , scroll_target = target.offset().top

  $(window).scrollTop(scroll_target - 10);
  return false
})

});
</script>

<div id="toc"></div>



    


    

    <a target="_blank" rel="noopener" href="https://github.com/aiegoo/documentation/pages/mydoc/mydoc_bebop_auto.md" class="btn btn-default githubEditButton" role="button"><i class="fa fa-github fa-lg"></i> Edit me</a>

    

   <hr />
<p>bebop_autonomy - ROS Driver for Parrot Bebop Drone (quadrocopter) 1.0 &amp; 2.0
<strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><em>**</em></p>

<p><em>bebop_autonomy</em> is a :abbr:<code class="language-plaintext highlighter-rouge">ROS (Robot Operating System)</code> driver for <code class="language-plaintext highlighter-rouge">Parrot Bebop 1.0 &lt;http://www.parrot.com/ca/products/bebop-drone/&gt;</code>_ and <code class="language-plaintext highlighter-rouge">2.0 &lt;https://www.parrot.com/ca/drones/parrot-bebop-2&gt;</code>_ drones (quadrocopters), based on Parrot’s official <code class="language-plaintext highlighter-rouge">ARDroneSDK3 &lt;http://developer.parrot.com/docs/SDK3/&gt;</code><em>. This driver has been developed in <code class="language-plaintext highlighter-rouge">Autonomy Lab &lt;http://autonomylab.org/&gt;</code></em> of <code class="language-plaintext highlighter-rouge">Simon Fraser University &lt;http://www.sfu.ca/&gt;</code>_ by <code class="language-plaintext highlighter-rouge">Mani Monajjemi &lt;http://mani.im&gt;</code>_ and other contributers (:ref:<code class="language-plaintext highlighter-rouge">sec-contribs</code>). This software is maintained by <code class="language-plaintext highlighter-rouge">Sepehr MohaimenianPour &lt;http://sepehr.im/&gt;</code>_ (AutonomyLab, Simon Fraser University), <code class="language-plaintext highlighter-rouge">Thomas Bamford &lt;#&gt;</code>_ (Dynamic Systems Lab, University of Toronto) and <code class="language-plaintext highlighter-rouge">Tobias Naegeli &lt;https://ait.ethz.ch/people/naegelit/&gt;</code>_ (Advanced Interactive Technologies Lab, ETH Zürich).</p>

<p>[<code class="language-plaintext highlighter-rouge">Source Code &lt;https://github.com/AutonomyLab/bebop_autonomy&gt;</code><em>] 
[<code class="language-plaintext highlighter-rouge">ROS wiki page &lt;http://wiki.ros.org/bebop_autonomy&gt;</code></em>] 
[<code class="language-plaintext highlighter-rouge">Support &lt;http://answers.ros.org/questions/scope:all/sort:activity-desc/tags:bebop_autonomy/page:1/&gt;</code><em>] 
[<code class="language-plaintext highlighter-rouge">Bug Tracker &lt;https://github.com/AutonomyLab/bebop_autonomy/issues&gt;</code></em>]</p>

<p>.. _sec-roadmap:</p>

<h1 id="features-and-roadmap">Features and Roadmap</h1>

<p>.. csv-table::
  :header: “Feature”, “Status”, “Notes”</p>

<p>SDK Version,”3.12.6”, “Since v0.7”
  Support for Parrot Bebop 1, Yes, “Tested up to Firmware 3.3”
  Support for Parrot Bebop 2, Yes, “Tested up to Firmware 4.0.6”
  Support for Parrot Disco FPV, No, “Not tested (help wanted)”
  Core piloting, Yes, “”
  H264 video decoding, Yes, “Enhancement: <code class="language-plaintext highlighter-rouge">#1 &lt;https://github.com/AutonomyLab/bebop_autonomy/issues/1&gt;</code><em>”
  ROS Camera Interface, Yes, “”
  Nodelet implementation, Yes, “”
  Publish Bebop states as ROS topics, Yes, “”
  Dynamically reconfigurable Bebop settings, Yes, “:ref:<code class="language-plaintext highlighter-rouge">sec-dev-dyn</code>”
  Use <code class="language-plaintext highlighter-rouge">parrot_arsdk &lt;https://github.com/AutonomyLab/parrot_arsdk&gt;</code></em> instead of building ARSDK3 inline, Yes, “Since v0.6: <code class="language-plaintext highlighter-rouge">#75 &lt;https://github.com/AutonomyLab/bebop_autonomy/issues/75&gt;</code>_”
  Bebop In The Loop tests, Yes, “:ref:<code class="language-plaintext highlighter-rouge">sec-dev-test</code>”
  Joystick teleop demo, Yes, “:ref:<code class="language-plaintext highlighter-rouge">sec-pilot-teleop</code>”
  TF Publisher, Yes, “Since v0.5 (:ref:<code class="language-plaintext highlighter-rouge">sec-tf</code>)”
  Odometry Publisher, Yes, “Since v0.5 (:ref:<code class="language-plaintext highlighter-rouge">sec-odom</code>)”
  Provide ROS API for on-board picture/video recording, Yes, “Since v0.4.1 (:ref:<code class="language-plaintext highlighter-rouge">sec-snapshot</code>)”
  GPS Support, Yes, “Since v0.6 (:ref:<code class="language-plaintext highlighter-rouge">sec-gps</code>)”
  Support for 720p streaming, Yes, “Since v0.6”
  Mavlink Support, No, “”
  Binary Release, No, “”
  Support for Parrot Sky Controller, No, “”</p>

<h1 id="table-of-contents">Table of Contents</h1>

<p>.. toctree::
  :maxdepth: 2</p>

<p>changelog
  installation
  running
  piloting
  reading
  configuration
  coordinates
  contribute
  FAQ
  dev
  license</p>

<h1 id="indices-and-tables">Indices and tables</h1>

<ul>
  <li>:ref:<code class="language-plaintext highlighter-rouge">genindex</code></li>
  <li>:ref:<code class="language-plaintext highlighter-rouge">modindex</code></li>
  <li>:ref:<code class="language-plaintext highlighter-rouge">search</code></li>
</ul>

<hr />

<hr />

<hr />
<p>Installation
<strong>**</strong><strong>**</strong></p>

<h1 id="compiling-from-source">Compiling From Source</h1>

<p>Pre-requirements:</p>

<ul>
  <li>ROS <em>Indigo</em>, <em>Jade</em> or <em>Kinetic</em> (Only tested on <em>Ubuntu</em>)</li>
  <li>Ubuntu packages: <code class="language-plaintext highlighter-rouge">build-esstential</code>, <code class="language-plaintext highlighter-rouge">python-rosdep</code>, <code class="language-plaintext highlighter-rouge">python-catkin-tools</code></li>
  <li>Basic familiarity with building ROS packages</li>
</ul>

<p>.. code-block:: bash</p>

<p>$ sudo apt-get install build-essential python-rosdep python-catkin-tools</p>

<p>To compile from source, you need to clone the source code in a new or existing <code class="language-plaintext highlighter-rouge">catkin</code> workspace, use <code class="language-plaintext highlighter-rouge">rosdep</code> to install dependencies and finally compile the workspace using <code class="language-plaintext highlighter-rouge">catkin</code>. The following commands demonstrate this procedure in a newly created <code class="language-plaintext highlighter-rouge">catkin</code> workspace.</p>

<p>.. note:: Since version 0.6, <code class="language-plaintext highlighter-rouge">Parrot ARSDK &lt;http://developer.parrot.com/docs/SDK3/&gt;</code><em>, the main underlying dependency of  *bebop_autonomy* is not build inline anymore. Instead, the slightly patched and catkinized version of it, called <code class="language-plaintext highlighter-rouge">parrot_arsdk &lt;https://github.com/AutonomyLab/parrot_arsdk&gt;</code></em>, is fetched as a dependency during the <code class="language-plaintext highlighter-rouge">rosdep install</code> step below. This dramatically decreases the compile time of the package compared to previous versions (e.g. from ~15 minutes to less than a minute on a modern computer). If you are re-compiling from source, you need to clean your workspace first: <code class="language-plaintext highlighter-rouge">$ catkin clean [-y]</code>.</p>

<p>.. code-block:: bash</p>

<p># Create and initialize the workspace
  $ mkdir -p ~/bebop_ws/src &amp;&amp; cd ~/bebop_ws
  $ catkin init
  $ git clone https://github.com/AutonomyLab/bebop_autonomy.git src/bebop_autonomy
  # Update rosdep database and install dependencies (including parrot_arsdk)
  $ rosdep update
  $ rosdep install –from-paths src -i
  # Build the workspace
  $ catkin build</p>

<hr />

<hr />

<hr />
<p>Running the Driver
<strong>**</strong><strong>**</strong><strong>**</strong></p>

<p>You can run Bebop’s ROS drivereither as a ROS <code class="language-plaintext highlighter-rouge">Nodelet &lt;http://wiki.ros.org/nodelet&gt;</code>_ or as a standalone ROS Node. The former is recommended if you intend to perform any kind of processing on Bebop’s video stream.</p>

<p>.. note:: If you compile the driver form source, do not forget to source your catkin workspace prior to running the driver. (i.e. <code class="language-plaintext highlighter-rouge">source ~/bebop_ws/devel/setup.[bash|zsh]</code>)</p>

<p>.. note:: Ensure that your Bebop’s firmware is at least <strong>2.0.29</strong> and your computer is connected to Bebop’s wireless network.</p>

<h1 id="running-the-driver-as-a-node">Running the driver as a Node</h1>

<p>The executable node is called <code class="language-plaintext highlighter-rouge">bebop_driver_node</code> and exists in <code class="language-plaintext highlighter-rouge">bebop_driver</code> package. It’s recommended to run the Node in its own namespace and with default configuration. The driver package comes with a sample launch file <code class="language-plaintext highlighter-rouge">bebop_driver/launch/bebop_node.launch</code> which demonstrates the procedure.</p>

<p>.. code-block:: bash</p>

<p>$ roslaunch bebop_driver bebop_node.launch</p>

<p>.. literalinclude::
  ../bebop_driver/launch/bebop_node.launch
  :language: XML
  :caption: bebop_node.launch</p>

<h1 id="running-the-driver-as-a-nodelet">Running the driver as a Nodelet</h1>

<p>To run the driver as a ROS Nodelet, you need to first run a Nodelet manager, then load the driver’s Nodelet (<code class="language-plaintext highlighter-rouge">bebop_driver/BebopDriverNodelet</code>) in it, along with other Nodelets that need to communicate with the driver. <code class="language-plaintext highlighter-rouge">bebop_tools/launch/bebop_nodelet_iv.launch</code> is a sample launch file that demonstrates these steps by visualizing Bebop’s video stream using an instance of <code class="language-plaintext highlighter-rouge">image_view/image &lt;http://wiki.ros.org/image_view#image_view.2BAC8-diamondback.image_view.2BAC8-image&gt;</code>_ Nodelet. Similar to <code class="language-plaintext highlighter-rouge">bebop_node.launch</code>, it also runs everything in its own namespace and loads the default configuration.</p>

<p>.. code-block:: bash</p>

<p>$ roslaunch bebop_tools bebop_nodelet_iv.launch</p>

<p>.. literalinclude::
  ../bebop_tools/launch/bebop_nodelet_iv.launch
  :language: XML
  :caption: bebop_tools/launch/bebop_nodelet_iv.launch</p>

<p>.. literalinclude::
  ../bebop_driver/launch/bebop_nodelet.launch
  :language: XML
  :caption: bebop_driver/launch/bebop_nodelet.launch</p>

<hr />

<hr />

<hr />
<p>Sending Commands to Bebop
<strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong>*</p>

<p>.. _sec-pilot-teleop:</p>

<p>.. note:: <code class="language-plaintext highlighter-rouge">bebop_tools</code> package comes with a launch file for tele-operating Bebop with a joystick using ROS <code class="language-plaintext highlighter-rouge">joy_teleop &lt;http://wiki.ros.org/joy_teleop&gt;</code>_ package. The configuration file (key-action map) is written for <code class="language-plaintext highlighter-rouge">Logitech F710 controller &lt;http://gaming.logitech.com/en-ca/product/f710-wireless-gamepad&gt;</code>_ and is located in <code class="language-plaintext highlighter-rouge">bebop_tools/config</code> folder. Adapting the file to your own controller is straightforward. To teleop Bebop while the driver is running execute <code class="language-plaintext highlighter-rouge">roslaunch bebop_tools joy_teleop.launch</code>.</p>

<h1 id="takeoff">Takeoff</h1>

<p>Publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty</code> to <code class="language-plaintext highlighter-rouge">takeoff</code> topic.</p>

<p>.. code-block:: bash</p>

<p>$ rostopic pub –once [namespace]/takeoff std_msgs/Empty</p>

<h1 id="land">Land</h1>

<p>Publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty</code> to <code class="language-plaintext highlighter-rouge">land</code> topic.</p>

<p>.. code-block:: bash</p>

<p>$ rostopic pub –once [namespace]/land std_msgs/Empty</p>

<h1 id="emergency">Emergency</h1>

<p>Publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty</code> to <code class="language-plaintext highlighter-rouge">reset</code> topic.</p>

<p>.. code-block:: bash</p>

<p>$ rostopic pub –once [namespace]/reset std_msgs/Empty</p>

<h1 id="piloting">Piloting</h1>

<p>To move Bebop around, publish messages of type <code class="language-plaintext highlighter-rouge">geometry_msgs/Twist &lt;http://docs.ros.org/api/geometry_msgs/html/msg/Twist.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">cmd_vel</code> topic while Bebop is flying. The effect of each field of the message on Bebop’s movement is listed below:</p>

<p>.. code-block:: text</p>

<p>linear.x  (+)      Translate forward
            (-)      Translate backward
  linear.y  (+)      Translate to left
            (-)      Translate to right
  linear.z  (+)      Ascend
            (-)      Descend
  angular.z (+)      Rotate counter clockwise
            (-)      Rotate clockwise</p>

<p>Acceptable range for all fields are <code class="language-plaintext highlighter-rouge">[-1..1]</code>. The drone executes the last received command as long as the driver is running. This command is reset to zero when Takeoff_, Land_ or Emergency_ command is received. To make Bebop hover and maintain its current position, you need to publish a message with all fields set to zero to <code class="language-plaintext highlighter-rouge">cmd_vel</code>.</p>

<p>The <code class="language-plaintext highlighter-rouge">linear.x</code> and <code class="language-plaintext highlighter-rouge">linear.y</code> parts of this message set the <strong>pitch</strong> and <strong>roll</strong> angles of the Bebop, respectively, hence control its forward and lateral accelerations. The resulting pitch/roll angles depend on the value of <code class="language-plaintext highlighter-rouge">~PilotingSettingsMaxTiltCurrent</code> <code class="language-plaintext highlighter-rouge">parameter &lt;./autogenerated/ardrone3_settings_param.html#pilotingsettingsmaxtiltcurrent&gt;</code>_, which is specified in degrees and is dynamically reconfigurable (:ref:<code class="language-plaintext highlighter-rouge">sec-dyn-params</code>).</p>

<p>The <code class="language-plaintext highlighter-rouge">linear.z</code> part of this message controls the <strong>vertical velocity</strong> of the Bebop. The resulting velocity in m/s depends on the value of <code class="language-plaintext highlighter-rouge">~SpeedSettingsMaxVerticalSpeedCurrent</code> <code class="language-plaintext highlighter-rouge">parameter &lt;./autogenerated/ardrone3_settings_param.html#speedsettingsmaxverticalspeedcurrent&gt;</code><em>, which is specified in meters per second and is also dynamically reconfigurable (:ref:<code class="language-plaintext highlighter-rouge">sec-dyn-params</code>). Similarly, the <code class="language-plaintext highlighter-rouge">angular.z</code> component of this message controls the rotational velocity of the Bebop (around the z-axis). The corresponding scaling <code class="language-plaintext highlighter-rouge">parameter &lt;./autogenerated/ardrone3_settings_param.html#speedsettingsmaxrotationspeedcurrent&gt;</code></em> is <code class="language-plaintext highlighter-rouge">SpeedSettingsMaxRotationSpeedCurrent</code> (in degrees per sec).</p>

<p>.. code-block:: text</p>

<p>roll_degree       = linear.y  * max_tilt_angle
  pitch_degree      = linear.x  * max_tilt_angle
  ver_vel_m_per_s   = linear.z  * max_vert_speed
  rot_vel_deg_per_s = angular.z * max_rot_speed</p>

<h1 id="moving-the-virtual-camera">Moving the Virtual Camera</h1>

<p>To move Bebop’s virtual camera, publish a message of type <code class="language-plaintext highlighter-rouge">geometry_msgs/Twist &lt;http://docs.ros.org/api/geometry_msgs/html/msg/Twist.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">camera_control</code> topic. <code class="language-plaintext highlighter-rouge">angular.y</code> and <code class="language-plaintext highlighter-rouge">angular.z</code> fields of this message set <strong>absolute</strong> tilt and pan of the camera in <strong>degrees</strong> respectively. The field of view of this virtual camera (based on our measurements) is ~80 (horizontal) and ~50 (vertical) degrees.</p>

<p>.. warning:: The API for this command is not stable. We plan to use <code class="language-plaintext highlighter-rouge">JointState</code> message in future versions.</p>

<p>.. code-block:: text</p>

<p>angular.y (+)      tilt down
            (-)      tilt up
  angular.z (+)      pan left
            (-)      pan right</p>

<h1 id="gps-navigation">GPS Navigation</h1>

<h2 id="start-flight-plan">Start Flight Plan</h2>

<p>An autonomous flight plan consists of a series of GPS waypoints along with Bebop velocities and camera angles encoded in an XML file.</p>

<p>Requirements that must be met before an autonomous flight can start:</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>* Bebop is calibrated
* Bebop is in outdoor mode
* Bebop has fixed its GPS
</code></pre></div></div>

<p>To start an autonomous flight plan, publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/String &lt;http://docs.ros.org/api/std_msgs/html/msg/String.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">autoflight/start</code> topic. The <code class="language-plaintext highlighter-rouge">data</code> field should contain the name of the flight plan to execute, which is already stored on-board Bebop.</p>

<p>.. note:: If an empty string is published, then the default ‘flightplan.mavlink’ is used.</p>

<p>.. warning:: If not already flying, Bebop will attempt to take off upon starting a flight plan.</p>

<p>The <code class="language-plaintext highlighter-rouge">Flight Plan App &lt;https://play.google.com/store/apps/details?id=com.parrot.freeflight3&gt;</code>_ allows easy construction of flight plans and saves them on-board Bebop.</p>

<p>An FTP client can also be used to view and copy flight plans on-board Bebop. <code class="language-plaintext highlighter-rouge">FileZilla</code> is recommended:</p>

<p>.. code-block:: bash</p>

<p>$ sudo apt-get install filezilla
  $ filezilla</p>

<p>Then open <code class="language-plaintext highlighter-rouge">Site Manager</code> (top left), click <code class="language-plaintext highlighter-rouge">New Site</code>:</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>* `Host`: 192.168.42.1
* `Protocol`: FTP
* `Encrpytion`: Use plain FTP
* `Logon Type`: Anonymous
* Connect.
</code></pre></div></div>

<h2 id="pause-flight-plan">Pause Flight Plan</h2>

<p>To pause the execution of an autonomous flight plan, publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty &lt;http://docs.ros.org/api/std_msgs/html/msg/Empty.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">autoflight/pause</code> topic. Bebop will then hover and await further commands.
To resume a paused flight plan, publish the same message that was used to start the autonomous flight (ie. to the topic <code class="language-plaintext highlighter-rouge">autoflight/start</code>). Bebop will fly to the lastest waypoint reached before continuing the flight plan.</p>

<p>.. note:: Any velocity commands sent to Bebop during an autonomous flight plan will pause the plan.</p>

<h2 id="stop-flight-plan">Stop Flight Plan</h2>

<p>To stop the execution of an autonomous flight plan, publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty &lt;http://docs.ros.org/api/std_msgs/html/msg/Empty.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">autoflight/stop</code> topic. Bebop will hover and await further commands.</p>

<h2 id="navigate-home">Navigate Home</h2>

<p>To ask Bebop to autonomously fly to it’s home position, publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Bool &lt;http://docs.ros.org/api/std_msgs/html/msg/Bool.html&gt;</code>_ to <code class="language-plaintext highlighter-rouge">autoflight/navigate_home</code> topic with the <code class="language-plaintext highlighter-rouge">data</code> field set to <code class="language-plaintext highlighter-rouge">true</code>. To stop Bebop from navigating home, publish another message with <code class="language-plaintext highlighter-rouge">data</code> set to <code class="language-plaintext highlighter-rouge">false</code>.</p>

<p>.. warning:: The topic has changed from <code class="language-plaintext highlighter-rouge">navigate_home</code> to <code class="language-plaintext highlighter-rouge">autoflight/navigate_home</code> after version 0.5.1.</p>

<h1 id="flat-trim">Flat Trim</h1>

<p>.. error:: Test fails, probably not working.</p>

<p>Publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/Empty</code> to <code class="language-plaintext highlighter-rouge">flattrim</code> topic.</p>

<p>.. code-block:: bash</p>

<p>$ rostopic pub –once [namespace]/flattrim std_msgs/Empty</p>

<h1 id="flight-animations">Flight Animations</h1>

<p>.. warning:: Be extra cautious when performing any flight animations, specially in indoor environments.</p>

<p>Bebop can perform four different types of flight animation (flipping). To perform an animation, publish a message of type <code class="language-plaintext highlighter-rouge">std_msgs/UInt8</code> to <code class="language-plaintext highlighter-rouge">flip</code> topic while drone is flying. The <code class="language-plaintext highlighter-rouge">data</code> field determines the requested animation type.</p>

<p>.. code-block:: text</p>

<p>0       Flip Forward
  1       Flip Backward
  2       Flip Right
  3       Flip Left</p>

<p>.. _sec-snapshot:</p>

<h1 id="take-on-board-snapshot">Take on-board Snapshot</h1>

<p>.. versionadded:: 0.4.1</p>

<p>To take a high resolution on-board snapshot, publish a <code class="language-plaintext highlighter-rouge">std_msgs/Empty</code> message on <code class="language-plaintext highlighter-rouge">snapshot</code> topic. The resulting snapshot is stored on the internal storage of the Bebop. The quality and type of this image is not configurable using the ROS driver. You can use the official FreeFlight3 app to configure your Bebop prior to flying. To access the on-board media, either connect your Bebop over USB to a computer, or use a FTP client to connect to your Bebop using the following settings:</p>

<ul>
  <li>Default IP: <code class="language-plaintext highlighter-rouge">192.168.42.1</code></li>
  <li>Port: <code class="language-plaintext highlighter-rouge">21</code></li>
  <li>Path: <code class="language-plaintext highlighter-rouge">internal_000/Bebop_Drone/media</code></li>
  <li>Username: <code class="language-plaintext highlighter-rouge">anonymous</code></li>
  <li>Password: *<no password="">*</no></li>
</ul>

<h1 id="set-camera-exposure">Set camera exposure</h1>

<p>It is possible to set camera exposure by publishing <code class="language-plaintext highlighter-rouge">std_msgs/Float32</code> message on <code class="language-plaintext highlighter-rouge">set_exposure</code> topic. Note that this functionality is not supported in Bebop1 Fw 3.3.0.</p>

<ul>
  <li>Exposure value range: <code class="language-plaintext highlighter-rouge">-3.0 .. +3.0</code></li>
</ul>

<h1 id="toggle-on-board-video-recording">Toggle on-board Video Recording</h1>

<p>.. versionadded:: 0.4.1</p>

<p>To start or stop on-board high-resolution video recording, publish a <code class="language-plaintext highlighter-rouge">std_msgs/Bool</code> message on the <code class="language-plaintext highlighter-rouge">record</code> topic. The value of <code class="language-plaintext highlighter-rouge">true</code> starts the recording while the value of <code class="language-plaintext highlighter-rouge">false</code> stops it. Please refer to the previous section for information on how to access the on-board recorded media.</p>

<hr />

<hr />

<hr />
<p>Reading from Bebop
<strong>**</strong><strong>**</strong><strong>**</strong></p>

<h1 id="camera">Camera</h1>

<p>The video stream from Bebop’s front camera is published on <code class="language-plaintext highlighter-rouge">image_raw</code> topic as <code class="language-plaintext highlighter-rouge">sensor_msgs/Image</code> messages. <em>bebop_driver</em> complies with ROS camera interface specifications and publishes camera information and calibration data to <code class="language-plaintext highlighter-rouge">camera_info</code> topic. Due to limitations in Parrot’s ARDroneSDK3, the quality of video stream is limited to <strong>640 x 368 @ 30 Hz</strong>. The field of view of this virtual camera (based on our measurements) is ~80 (horizontal) and ~50 (vertical) degrees.</p>

<p>To set the location of camera calibration data, please check this page: :doc:<code class="language-plaintext highlighter-rouge">configuration</code>. Since v0.4, the package ships with a default camera caliberation file located at <code class="language-plaintext highlighter-rouge">bebop_driver/data/bebop_front_calib.yaml</code>. Both default node/nodelet launch files, load this file when executing the driver.</p>

<p>.. _sec-ros-topic:</p>

<h1 id="standard-ros-messages">Standard ROS messages</h1>

<p>.. _sec-odom:</p>

<h2 id="odometery">Odometery</h2>

<p>.. versionadded:: 0.5</p>

<ul>
  <li>ROS Topic: <code class="language-plaintext highlighter-rouge">odom</code></li>
  <li>ROS Message Type: <code class="language-plaintext highlighter-rouge">nav_msgs/Odometry</code></li>
</ul>

<p>The driver integerates visual-inertial velocity estimates reported by Bebop’s firmware to calculate the odometery. This message contains both the position and velocity of the Bebop in an ENU aligned odometery frame also named as <code class="language-plaintext highlighter-rouge">odom</code>. This frame name is configurable (see :ref:<code class="language-plaintext highlighter-rouge">sec-params</code>) The cooridnate frame convention complies with ROS REP 103 (:ref:<code class="language-plaintext highlighter-rouge">sec-coords</code>). Please not that since odometery is calculated from Bebop States (see :ref:<code class="language-plaintext highlighter-rouge">sec-states</code>), the update rate is limited to <strong>5 Hz</strong>.</p>

<p>.. _sec-gps:</p>

<h2 id="gps">GPS</h2>

<p>.. versionadded:: 0.5</p>

<ul>
  <li>ROS Topic: <code class="language-plaintext highlighter-rouge">fix</code></li>
  <li>ROS Message Type: <code class="language-plaintext highlighter-rouge">sensor_msgs/NavSatFix</code></li>
</ul>

<h2 id="joint-states-pantilt-of-the-virtual-camera">Joint States (Pan/Tilt of The Virtual Camera)</h2>

<p>.. versionadded:: 0.5</p>

<ul>
  <li>ROS Topic: <code class="language-plaintext highlighter-rouge">joint_states</code></li>
  <li>ROS Message Type: <code class="language-plaintext highlighter-rouge">sensor_msgs/JointState</code></li>
</ul>

<p>.. _sec-tf:</p>

<h1 id="tf">TF</h1>

<p>.. versionadded:: 0.5</p>

<p>The driver updates the following <code class="language-plaintext highlighter-rouge">TF &lt;http://wiki.ros.org/tf&gt;</code>_ tree based on a simple kinematic model of the Bebop (provided by <code class="language-plaintext highlighter-rouge">bebop_description</code>) pacakge, the current state of the virtual camera joints and the calculated odometery (if <code class="language-plaintext highlighter-rouge">publish_odom_tf</code> is set, see :ref:<code class="language-plaintext highlighter-rouge">sec-params</code>).</p>

<p>.. image:: img/tf.png</p>

<p>.. _sec-states:</p>

<p><img src="https://github.com/AutonomyLab/bebop_autonomy/raw/indigo-devel/docs/img/tf.png" alt="odom_tf" />
States (aka Navdata)</p>

<p>====================</p>

<p>Unlike Parrot ARDrone, Bebop does not constantly transmit all on-board data back to the host device with high frequency. Each state variable is sent only when its value is changed. In addition, the publication rate is currently limited to <strong>5 Hz</strong>. The driver publishes these states <strong>selectively</strong> and when <strong>explicitly</strong> enabled through a ROS parameter. For example setting <code class="language-plaintext highlighter-rouge">~states/enable_pilotingstate_flyingstatechanged</code> parameter to <code class="language-plaintext highlighter-rouge">true</code> will enable the publication of flying state changes to topic <code class="language-plaintext highlighter-rouge">states/ARDrone3/PilotingState/FlyingStateChanged</code>. List of all such parameters and their corresponding topics and message types are indexed in the following pages:</p>

<p>Common States
  :doc:<code class="language-plaintext highlighter-rouge">autogenerated/common_states_param_topic</code>
Bebop-specific States
  :doc:<code class="language-plaintext highlighter-rouge">autogenerated/ardrone3_states_param_topic</code></p>

<hr />

<hr />

<hr />
<p>Configuring Bebop and the Driver
<strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong>**</p>

<p>.. _sec-params:</p>

<h1 id="driver-parameters">Driver Parameters</h1>

<p>Following parameters are set during driver’s startup:</p>

<h2 id="bebop_ip">~bebop_ip</h2>

<p>Sets the IP addres of the Bebop. The default value is <code class="language-plaintext highlighter-rouge">192.168.42.1</code>.</p>

<h2 id="reset_settings">~reset_settings</h2>

<p>Setting this parameter to <code class="language-plaintext highlighter-rouge">true</code> will reset all Bebop configurations to factory defaults. Default value is <code class="language-plaintext highlighter-rouge">false</code>.</p>

<h2 id="sync_time">~sync_time</h2>

<p>Setting this parameter to <code class="language-plaintext highlighter-rouge">true</code> will synchronize drone time with your ROS system time. Default value is <code class="language-plaintext highlighter-rouge">false</code>.</p>

<h2 id="camera_info_url">~camera_info_url</h2>

<p>Sets the location of the camera calibration data. Default is empty string. For more information check <code class="language-plaintext highlighter-rouge">this documentation &lt;http://wiki.ros.org/camera_info_manager#URL_Names&gt;</code>_.</p>

<p>.. note::</p>

<p>Since v0.4, the package comes with a default camera calibration file located at <code class="language-plaintext highlighter-rouge">bebop_driver/data/bebop_front_calib.yaml</code>.</p>

<h2 id="cmd_vel_timeout">~cmd_vel_timeout</h2>

<p>.. versionadded:: 0.4</p>

<p>Sets the safety timeout for piloting <code class="language-plaintext highlighter-rouge">cmd_vel</code> commands in seconds. Deafult is set to <strong>0.1</strong> seconds (100 miliseconds). If no piloting command is received by the driver within this timeout period, the driver issues a stop command which causes the drone to hover.</p>

<h2 id="odom_frame_id">~odom_frame_id</h2>

<p>.. versionadded:: 0.5</p>

<p>Sets the <code class="language-plaintext highlighter-rouge">frame_id</code> of the odometery message (see :ref:<code class="language-plaintext highlighter-rouge">sec-ros-topic</code>) and the odometery frame used in the TF tree (see :ref:<code class="language-plaintext highlighter-rouge">sec-tf</code>). The default value is <code class="language-plaintext highlighter-rouge">odom</code>.</p>

<h2 id="publish_odom_tf">~publish_odom_tf</h2>

<p>.. versionadded:: 0.5</p>

<p>Enables the publishing of <code class="language-plaintext highlighter-rouge">odom</code> to <code class="language-plaintext highlighter-rouge">base_link</code> TF transform (see :ref:<code class="language-plaintext highlighter-rouge">sec-tf</code>). The default value is <code class="language-plaintext highlighter-rouge">true</code>.</p>

<h2 id="camera_frame_id">~camera_frame_id</h2>

<p>.. deprecated:: 0.5</p>

<p>Sets the <code class="language-plaintext highlighter-rouge">frame_id</code> of camera and image messages. The default value is <code class="language-plaintext highlighter-rouge">camera_optical</code>.</p>

<p>.. _sec-dyn-params:</p>

<h1 id="dynamically-reconfigurable-parameters-for-bebop">Dynamically Reconfigurable Parameters for Bebop</h1>

<p>Following ROS parameters change Bebop’s settings. They can be tweaked during runtime using <code class="language-plaintext highlighter-rouge">dynamic reconfigure GUI &lt;http://wiki.ros.org/dynamic_reconfigure#dynamic_reconfigure.2BAC8-groovy.reconfigure_gui&gt;</code><em>. Setting <code class="language-plaintext highlighter-rouge">~reset_settings</code></em> parameter to <code class="language-plaintext highlighter-rouge">true</code> will reset all these settings to factory defaults.</p>

<p>:doc:<code class="language-plaintext highlighter-rouge">autogenerated/ardrone3_settings_param</code></p>

<hr />

<hr />

<hr />
<p>Coordinate System Conventions
<strong>**</strong><strong>**</strong><strong>**</strong><strong>**</strong>*****</p>

<p>.. _sec-coords:</p>

<h1 id="ros-standard-message-types-ie-twist-odometery---rep-103">ROS Standard Message Types (i.e Twist, Odometery) - REP 103</h1>

<p>+x    forward
+y    left
+z    up
+yaw  CCW</p>

<ul>
  <li>More information: http://www.ros.org/reps/rep-0103.html</li>
</ul>

<h1 id="bebop-velocities">Bebop Velocities</h1>

<p>+x    East
+y    South
+z    Down</p>

<h1 id="bebop-attitude">Bebop Attitude</h1>

<p>+x    forward
+y    right
+z    down
+yaw  CW</p>

<h1 id="sdks-setpilotingpcmd">SDK’s setPilotingPCMD</h1>

<p>+roll   right
+pitch  forward
+gaz    up
+yaw    CW</p>

<hr />

<hr />

<hr />
<p>Under The Hood
<strong>**</strong><strong>**</strong>**</p>

<p>This page contains information about the architecture of the driver and different techniques used for its development.</p>

<h1 id="automatic-code-generation">Automatic Code Generation</h1>

<p>TBA</p>

<h1 id="threading-model">Threading Model</h1>

<p>TBA</p>

<h1 id="publishing-the-states">Publishing the States</h1>

<p>TBA</p>

<p>.. _sec-dev-dyn:</p>

<h1 id="configuring-the-drone">Configuring the Drone</h1>

<p>TBA</p>

<p>.. _sec-dev-test:</p>

<h1 id="tests">Tests</h1>

<h2 id="enabling-bebop-in-the-loop-tests">Enabling Bebop In The Loop Tests</h2>

<p>.. code-block:: bash</p>

<p>$ cd /path/to/bebop_ws
  $ catkin clean –cmake-cache
  $ catkin build bebop_driver –cmake-args -DRUN_HARDWARE_TESTS=ON</p>

<h2 id="running-bebop-in-the-loop-tests">Running Bebop In The Loop Tests</h2>

<p>.. warning:: Bebop in the loop tests perform live unit tests with a real robot. Please proceed with caution and execute the tests in an area with at least 5 meters of clearance radius (empty space) around the Bebop.</p>

<p>.. code-block:: bash</p>

<p>$ cd /path/to/bebop_ws/build/bebop_driver
  $ make tests
  $ rostest –text bebop_driver bebop_itl_test.test</p>

<h1 id="upgrading-the-bebop-sdk">Upgrading the Bebop SDK</h1>

<p>.. warning:: Since version 0.6, <code class="language-plaintext highlighter-rouge">Parrot ARSDK &lt;http://developer.parrot.com/docs/SDK3/&gt;</code><em>, the main underlying dependency of  *bebop_autonomy* is not build inline anymore. Instead, the slightly patched and catkinized version of it, called <code class="language-plaintext highlighter-rouge">parrot_arsdk &lt;https://github.com/AutonomyLab/parrot_arsdk&gt;</code></em>, is fetched as a dependency. <strong>The following documentation needs to be updated</strong>.</p>

<ol>
  <li>Update the <code class="language-plaintext highlighter-rouge">GIT_TAG</code> of <code class="language-plaintext highlighter-rouge">ARDroneSDK3</code> in <code class="language-plaintext highlighter-rouge">bebop_driver/CMakeLists.txt::add_custom_target::./repo init ... -b GIT_TAG</code> to your desired commit hash, branch or tag (release). The official upstream repository is hosted <code class="language-plaintext highlighter-rouge">here &lt;https://github.com/Parrot-Developers/arsdk_manifests&gt;</code>_.</li>
  <li>Checkout (or browse) the upstream repository at the same hash used in step (1) and open <code class="language-plaintext highlighter-rouge">release.xml</code> file. From this file, extract the commit hash of <code class="language-plaintext highlighter-rouge">arsdk-xml</code> from the <code class="language-plaintext highlighter-rouge">revision</code> property of this XML tag: <code class="language-plaintext highlighter-rouge">&lt;project name="arsdk-xml" ... revision="" /&gt;</code>.</li>
  <li>Open <code class="language-plaintext highlighter-rouge">bebop_driver/scripts/meta/generate.py</code> and update <code class="language-plaintext highlighter-rouge">LIBARCOMMANDS_GIT_HASH</code> variable to the hash obtained in step (2).</li>
  <li>Change the working diretory to <code class="language-plaintext highlighter-rouge">bebop_driver/scripts/meta</code>, then execute <code class="language-plaintext highlighter-rouge">generate.py</code> from the command line. This will regenerate all automatically generated message definitions, header files and documentations.</li>
  <li>Copy the generated files to their target locations by calling <code class="language-plaintext highlighter-rouge">./install.sh</code>.</li>
  <li>In <code class="language-plaintext highlighter-rouge">bebop_driver/include/bebop_driver/autogenerated/ardrone3_setting_callbacks.h</code> change the following varialbles:</li>
</ol>

<ul>
  <li><code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_MAXDISTANCECHANGED_VALUE</code> to <code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_MAXDISTANCECHANGED_CURRENT</code>.</li>
  <li><code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_BANKEDTURNCHANGED_VALUE</code> to <code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_BANKEDTURNCHANGED_STATE</code></li>
  <li><code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_CIRCLINGRADIUSCHANGED_VALUE</code> to <code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_CIRCLINGRADIUSCHANGED_CURRENT</code></li>
  <li><code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_CIRCLINGALTITUDECHANGED_VALUE</code> to <code class="language-plaintext highlighter-rouge">ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_PILOTINGSETTINGSSTATE_CIRCLINGALTITUDECHANGED_CURRENT</code></li>
</ul>

<p>In <code class="language-plaintext highlighter-rouge">bebop_driver/include/bebop_driver/autogenerated/ardrone3_state_callbacks.h</code> remove the following lines:</p>

<p><code class="language-plaintext highlighter-rouge">arg = NULL;
    HASH_FIND_STR (arguments, ARCONTROLLER_DICTIONARY_KEY_ARDRONE3_ACCESSORYSTATE_CONNECTEDACCESSORIES_LIST_FLAGS, arg);
    if (arg)
    {
      msg_ptr-&gt;list_flags = arg-&gt;value.U8;
    }</code></p>

<p>In <code class="language-plaintext highlighter-rouge">bebop_msgs/msg/autogenerated/Ardrone3AccessoryStateConnectedAccessories.msg</code> remove the following lines:
  <code class="language-plaintext highlighter-rouge"># List entry attribute Bitfield. 0x01: First: indicate its the first element of the list. 0x02: Last: indicate its the last element of the list. 0x04: Empty: indicate the list is empty (implies First/Last). All other arguments should be ignored. 0x08: Remove: This value should be removed from the existing list.
    uint8 list_flags</code></p>

<p>These changes are required because the upstream XML file is inconsistent for a couple of variable names.</p>

<ol>
  <li>Remove <code class="language-plaintext highlighter-rouge">build</code> and <code class="language-plaintext highlighter-rouge">devel</code> space of your <code class="language-plaintext highlighter-rouge">catkin</code> workspace, then re-build it.</li>
</ol>


    <div class="tags">
        
    </div>


<div id="commento"></div>
<script src="https://cdn.commento.io/js/commento.js"></script>
<noscript>Please enable JavaScript to load the comments.</noscript>






</div>

<hr class="shaded"/>

<footer>
            <div class="row">
                <div class="col-lg-12 footer">
               &copy;2021 Copyright 2021 Tonyleekorea. All rights reserved. <br />
 Site last generated: Jul 7, 2021 <br />
<p><img src="images/company_logo.png" alt="Company logo"/></p>
                </div>
            </div>
</footer>






        </div>
    <!-- /.row -->
</div>
<!-- /.container -->
</div>
<!-- /#main -->
    </div>

</body>

</html>


