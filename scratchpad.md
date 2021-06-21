 wget https://github.com/actions/actions-sync/releases/download/v202009231612/gh_202009231612_linux_amd64.tar.gz 
tar xvfz gh_202009231612_linux_amd64.tar.gz 
 ./actions-sync --cache-dir=/tmp/actions pull --repo-name jonico/action-cats 
