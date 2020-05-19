<table>
  <tr>
    <td><a href="https://philip-sul.github.io">Projects</a></td>
    <td><a href="https://philip-sul.github.io/blog">Blog</a></td>
  </tr>
</table>

# My Blog
<hr>

## Issue: Markdown issue with multiple lists on single page
### Fix: Use Block or inline elements such as div to separate lists - 05.19.2020

Issue:

Was adding bullet points descriptions under some pictures and realized it was breaking my page.
Did not find a recent fix on stack overflow so played with the html.

But basically Markdown might interpret seperate lists on a page as one list.

The fix is to use html and make sure it is enclosed in a container like a div:

    <div>
      <ul>
         <li>Google Location API asking for your location.</li>
         <li>It will result in something like the first image (above).</li>
      </ul>
    </div>

<hr>

## Issue: Roslyn issue when running MVC project
### Fix: Outdated packages - 05.08.2020

Issue:

Trying to run project after first time in about a year.
Had an issue with <i>Could not find a part of the path … bin\roslyn\csc.exe</i>

Run this in the Package Manager Console:

    Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r

[https://stackoverflow.com/questions/32780315/could-not-find-a-part-of-the-path-bin-roslyn-csc-exe](https://stackoverflow.com/questions/32780315/could-not-find-a-part-of-the-path-bin-roslyn-csc-exe)

Basically some .NET packages had bugs and they were updated.

<hr>

## Issue: Resizing images on github 
### Fix: Use absolute path from Chrome Dev Tools - 05.08.2020

I was looking for a quick way to resize images in Markdown.
There are some outdated solutions on the web.

I found a gist that led me to the solution:
[image resize gist](https://gist.github.com/uupaa/f77d2bcf4dc7a294d109)

It said to find the src using Chrome Dev Tools

Working example:

    <img src="https://github.com/philip-sul/philip-sul.github.io/raw/master/images/location_page_load.png" alt="location page load graph" height="75%" width="75%">

The solution is to use an absolute file path.

I was having issues because the regular way to add images in Markdown is using relative file path:

    ![location page load graph](/images/location_page_load.png)

I also was reading in the Markdown documentation that you can use html inline so I knew it should be working and narrowed it down
to and issue with the src.

<img src="https://github.com/philip-sul/philip-sul.github.io/raw/master/images/location_page_load.png" alt="location page load graph" height="75%" width="75%">

:)

<hr>

## First Blog post 
### Github portfolio - 05.08.2020

I have started to upload some of my school projects publically to Github last week.
Some previously localhost or privately on Github or Bitbucket.

I will track my progress here with a simple blog to reflect on my achievements and struggles.

<hr>
