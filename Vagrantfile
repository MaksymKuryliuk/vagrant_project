Vagrant.configure("2") do |config|
  # Веб-сервер
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/focal64"
    web.vm.network "forwarded_port", guest: 80, host: 8080
    web.vm.hostname = "web"
  end

  # Сервер бази даних
  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/focal64"
    db.vm.network "forwarded_port", guest: 3306, host: 3306
    db.vm.hostname = "db"
  end
end
 
