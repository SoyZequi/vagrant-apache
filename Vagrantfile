Vagrant.configure("2") do |config|
    config.vm.define "pag1" do |web1|
      web1.vm.provider "docker" do |d|
        d.image = "ubuntu:20.04"
        d.has_ssh = false
        d.remains_running = true
        d.cmd = ["bash", "-c", "apt-get update && apt-get install -y apache2 && echo '<html><body><h1>Hola Mundo desde web1</h1></body></html>' > /var/www/html/index.html && apachectl -D FOREGROUND"]
        d.ports = ["8080:80"]
      end
    end
  
    config.vm.define "pag2" do |web2|
      web2.vm.provider "docker" do |d|
        d.image = "ubuntu:20.04"
        d.has_ssh = false
        d.remains_running = true
        d.cmd = ["bash", "-c", "apt-get update && apt-get install -y apache2 && echo '<html><body><h1>Hola Mundo desde web2</h1></body></html>' > /var/www/html/index.html && apachectl -D FOREGROUND"]
        d.ports = ["8081:80"]
      end
    end
  end
  
