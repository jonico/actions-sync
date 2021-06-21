
```bash
cd
mkdir -p /tmp/actions
git clone https://github.com/github/platform-samples.git
sdk install groovy
cd platform-samples/api/groovy/
groovy ListReposInOrg.groovy -t $GH_PUBLIC actions > ~/repo-list

cd
wget https://github.com/actions/actions-sync/releases/download/v202009231612/gh_202009231612_linux_amd64.tar.gz 
tar xvfz gh_202009231612_linux_amd64.tar.gz 

cd bin/
./actions-sync --cache-dir=/tmp/actions pull --repo-name jonico/action-cats 
./actions-sync --cache-dir=/tmp/actions pull --repo-name-list-file ~/repo-list 
./actions-sync --cache-dir=/tmp/actions --destination-url "https://octodemo.com" --destination-token=$ACTIONS_SYNC push
```
 