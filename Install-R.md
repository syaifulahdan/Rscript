###How to Install R on Linux Ubuntu 16.04 Xenial Xerus

Source from : http://www.tutorialspoint.com/r/ 
https://www.r-bloggers.com/how-to-install-r-on-linux-ubuntu-16-04-xenial-xerus/

R is a programming language and software environment for statistical analysis, graphics representation and reporting. R was created by Ross Ihaka and Robert Gentleman at the University of Auckland, New Zealand, and is currently developed by the R Development Core Team.

R is freely available under the GNU General Public License, and pre-compiled binary versions are provided for various operating systems like Linux, Windows and Mac.

This programming language was named R, based on the first letter of first name of the two R authors (Robert Gentleman and Ross Ihaka), and partly a play on the name of the Bell Labs Language S.

The long-awaited new Ubuntu LTS Xenial Xerus was released last week. I wrote a tutorial on installing R and R-Studio on the old 14.04 LTS, so I figured I’d update that document. Not much has changed for the new 16.04 version but there are new repositories.

<b>Install R-Base</b>

You can find R-Base in the Software Center; this would be the easy way to do it. However, the Software Center versions are often out of date, which can be a pain moving foward when your packages are based on the most current version of R Base. The easy fix is to download and install R Base directly from the Cran servers.


<b>1. Add R repository</b>

First, we’ve got to add a line to our /etc/apt/sources.list file. This can be accomplished with the following. Note the “xenial” in the line, indicating Ubuntu 16.04. If you have a different version, just change that.

<pre>sudo echo "deb http://cran.rstudio.com/bin/linux/ubuntu xenial/" | sudo tee -a /etc/apt/sources.list</pre>

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-19%2017-13-21.png)

<b>2. Add R to Ubuntu Keyring</b>

First:

 <pre>gpg --keyserver keyserver.ubuntu.com --recv-key E084DAB9</pre>.
 
Then:

 <pre>gpg -a --export E084DAB9 | sudo apt-key add -</pre>

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-19%2017-19-50.png)

<b>3. Install R-Base</b>

Most Linux users should be familiar with the old…
<pre> sudo apt-get update</pre>

<pre>sudo apt-get install r-base r-base-dev</pre>

![alt tag](https://github.com/syaifulahdan/Rscript/blob/master/image/Screenshot%20from%202016-09-19%2017-35-54.png)

<b>Installing R-Studio</b>

From here you can download your files and install the IDE through Ubuntu Software Center or Synaptic Package Manager, or since you’ve already got the terminal open, you could just:

<pre>
sudo apt-get install gdebi-core
wget https://download1.rstudio.org/rstudio-0.99.896-amd64.deb
sudo gdebi -n rstudio-0.99.896-amd64.deb
rm rstudio-0.99.896-amd64.deb
</pre>
