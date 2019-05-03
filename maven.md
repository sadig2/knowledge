sudo tar -xvzf apache-maven-3.3.9-bin.tar.gz -C /opt


As a result Maven will be extracted into the /opt/apache-maven-3.3.9 folder.
Rename folder apache-maven-3.3.9 to maven:
sudo mv /opt/apache-maven-3.3.9 /opt/maven


To use maven from the console (terminal) we need to edit the .bashrc file and add the following lines:
# =======  maven settings =========
export M2_HOME=/opt/maven/
export M2=$M2_HOME/bin
export PATH=$M2:$PATH


Reload .bashrc:
source ~/.bashrc


Verify that everything works correct:
mvn -v

mvn archetype:generate

cd pom directory

mvn compile


