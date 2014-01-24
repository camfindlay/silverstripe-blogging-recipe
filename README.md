# SilverStripe Blogging Recipe
##Author/Chef
Cam Findlay <cam@silverstripe.com>

##Ingredients
The blogging recipe requires:

    "silverstripe/cms": "~3.1",
    "silverstripe/framework": "~3.1",
    "silverstripe-themes/simple": "*",	
    "silverstripe-themes/simple_blog": "*",
    "silverstripe/userforms": "*",
    "silverstripe/blog": "*",
    "silverstripe/comments": "*",
    "silverstripe/widgets": "*",
    "silverstripe/spamprotection": "*",
    "tractorcow/silverstripe-akismet": "3.1.*@dev",
    "simplepie/simplepie": "*",
    "ezyang/htmlpurifier": "4.*"

##Installation
###Install via composer
    composer require camfindlay/blogging-recipe dev-master

###Akismet Spam Setup
Create an Akisment API key at [https://akismet.com](https://akismet.com) (Free for non-commercial use).

Add to your *mysite/_config/config.yml* or any other config method defined in the SilverStripe Akismet module documentation.
    AkismetSpamProtector:
      api_key: <insert-akisment-key-here>

###Run dev/build
    sake dev/build flush=1

*Note: there is some configuration that is assumed in this recipes to enable the widgets and Akismet spam protection for use on your blog.

If you don't like this configuration... create your own recipe and share it!!

##What this recipe does
This SilverStripe recipe module can be composer required into a clean installation of SilverStripe and will pull in a pre-selected set of SilverStripe modules and themes suitable for starting a blog website. 

Where you customise from there is up to you.


##License
Copyright (c) 2014, Cam Findlay
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.