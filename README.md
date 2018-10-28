# quick_start_linux_mint_19

<h1>install driver for the wifi card</h1>
<p>#to get the name of the wifi card</p>
<p>lspci | grep -i network</p>
<p>sudo apt install bcmwl-kernel-source</p>


<h1>install docker</h1>
<p>#delet old versions</p>
<p>sudo apt-get remove docker docker-engine docker.io</p>

<p>#Update the apt package index</p>
<p>sudo apt-get update</p>

<p>#Install packages to allow apt to use a repository over HTTPS</p>
<p>sudo apt-get install apt-transport-https ca-certificates curl software-properties-common</p>

<p>#Add Docker’s official GPG key</p>
<p>curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -</p>

<p>#Up the stable repository of Docker. NB : Change the $V variable relative to the version on which your system is based for linux mint ==> Stretch/Trusty/Xenial/ bionic</p>
<p>V=bionic</p>
<p>sudo add-apt-repository "deb [arch=amd64]https://download.docker.com/linux/ubuntu $V stable"</p>

<p>#Update the apt package index</p>
<p>sudo apt-get update</p>

<p>#Install Docker CE</p>
<p>sudo apt-get install docker-ce</p>

<p>#teste docker</p>
<p>#sudo docker run hello-world</p>

<p>#to use the docker without the sudo we have to add it to the user group</p>
<p>#Create the docker group.</p>
<p>sudo groupadd docker</p>

<p>#Add your user to the docker group.</p>
<p>sudo usermod -aG docker $USER</p>
<p>relog</p>
