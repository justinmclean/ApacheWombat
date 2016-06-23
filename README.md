## Apache&reg; Wombat

This is a demonstration in how to assemble the LICENSE and NOTICE files for a fictional project at the [Apache Software Foundation][12] called Apache Wombat.

When assembling LICENSE and NOTICE file please to refer to the [assembling how to][1] and the [ASF Legal resolved questions][2].

A release of Apache Wombat would consists of all the files contained in this repository which is a copy of bootstrap.

Firstly add boilerplate LICENSE and NOTICE files to the project.
One way to get these files is from the Apache website like so:  
`curl http://www.apache.org/licenses/LICENSE-2.0.txt > LICENSE`
`curl http://www.apache.org/licenses/NOTICE-2.0.txt > NOTICE`

Edit the NOTICE file to include the project name (Apache Wombat) and year of copyright (currently 2016).

Bootstrap is licensed under a permissive [MIT licence][3]. This is listed at a Category A permissive license [compatible with the Apache 2.0 License][16].

Save the license text and [add a pointer][13] to this file to LICENSE.

`curl https://raw.githubusercontent.com/twbs/bootstrap/v3.3.2/LICENSE > licenses/bootstrap.MIT`

As this is the first component added to LICENSE a little more text is needed:

>   APACHE WOMBAT SUBCOMPONENTS:
>
>   The Apache Wombat includes a number of subcomponents with
>   separate copyright notices and license terms. Your use of the source
>   code for the these subcomponents is subject to the terms and
>   conditions of the following licenses. 
>
>   This product bundles Bootstrap 3.3.6, copyright Twitter, Inc.,
>   which is available under a MIT license.
>   For details, see licenses/bootstrap.MIT.

It's always a good idea to mention the product version in the license pointer as licenses may differ between versions of a product and have done in the bootstrap project.

Next looking at the index.html you can see a number of references to other JavaScript frameworks and code. They include [HTML5 shiv][4], [Respond.js][6] and [jQuery][8].

HTML5 shiv is [dual license under MIT and GPL][5]. GPL is a category X license and can't be used as a dependency in an Apache project. When something is dual licensed you can take the [most permissive licence and use that][14]. In this case select the more permissive MIT license. As HTML5 shiv would not be bundled in a release [nothing needs to be added][15] to LICENSE or NOTICE.

Respond.js is [MIT licensed][9]. Again as it is not bundled so [nothing needs to be added][15] to LICENSE or NOTICE. JQuery is also [MIT licensed][9] and again [nothing needs to be done][15].

All these pieces are permissively licensed (Category A) so there are [no licensing issues][17] with any of the dependencies.

Looking inside bootstrap.css you can see that it includes normalize.css. Normalize.css is [MIT licensed][10] and as this is bundled it [needs to be added][13] to LICENSE. Download the license file and add a licence pointer to LICENSE to point to that license.

`curl https://raw.githubusercontent.com/necolas/normalize.css/master/LICENSE.md  > licenses/normalize.MIT`

>   This product bundles normalize 3.0.3 copyright Nicolas Gallagher and
>   Jonathan Neal, which is available under a MIT license.
>   For details, see licenses/normalize.MIT.

Also inside the fonts directory is glyphicons halflings font this is normally a commercial paid for product but is [licensed under MIT][11] when used in bootstrap. There's no license file so one way to deal with this is to create one for it adding the copyright owner. After the license file has been created [add a pointer][13] to it in the LICENSE file.

>   This product bundles Glyphicons Halflings Regular, copyright
>   Jan Kovarik, which is available under a MIT license.
>   For details, see licenses/glyphicons.MIT.

<sup>Apache is a trademark of The Apache Software Foundation.</sup>


[1]:http://www.apache.org/dev/licensing-howto.html
[2]:http://www.apache.org/legal/resolved.html
[3]:https://github.com/twbs/bootstrap/blob/v3.3.2/LICENSE
[4]:https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js
[5]:https://github.com/aFarkas/html5shiv/blob/master/MIT%20and%20GPL2%20licenses.md
[6]:https://oss.maxcdn.com/respond/1.4.2/respond.min.js
[7]:https://github.com/scottjehl/Respond/blob/master/LICENSE-MIT
[8]:https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js
[9]:https://jquery.org/license/
[10]:https://github.com/necolas/normalize.css/blob/master/LICENSE.md
[11]:http://glyphicons.com/license/
[12]:http://www.apache.org
[13]:http://www.apache.org/dev/licensing-howto.html#permissive-deps
[14]:http://www.apache.org/legal/resolved.html#mutually-exclusive
[15]:http://www.apache.org/dev/licensing-howto.html#guiding-principle
[16]:http://www.apache.org/legal/resolved.html#category-a
[17]:http://www.apache.org/legal/resolved.html#prohibited

