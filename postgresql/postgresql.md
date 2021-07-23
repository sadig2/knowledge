# install postgres into mac m1

1. # install postgresl from brew
    brew install postgres
2. # create symlinks with right directories
    ln -sfv /opt/homebrew/opt/postgresql/*.plist ~/Library/LaunchAgents
alias pg_start="launchctl load ~/Library/LaunchAgents"
alias pg_stop="launchctl unload ~/Library/LaunchAgents"

3. install 
brew install openssl