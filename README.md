# Advance-recon

1 find subdomains of target from different tools || google dorks
google dorks:
site: *.hackerone.com

site: ..hackerone.com

sublis3r
sublist3r -d domain-name

dnsrecon :
dnsrecon -d hackerone.com -D ~/wordlists/subdomains.txt -t brt

subfinder
subfinder

2 How to organise work for bug bounty
software for organizing the work: xmind

JASON HADIX TEMPLATE

3 directry fuzzing or content finding (ffuz), httprobe , byp4xx
usefull wordlist if needed (wordlist are already in kali linux seclists but if you need more then checkout): USEFUL WORDLIST

HTTPROBE

 git clone https://github.com/tomnomnom/httprobe
FFUZ

git clone https://github.com/ffuf/ffuf
most used ffuz command :

ffuf -p 0.1 -t 1 -w ~/wordlists/content.txt -u https://www.website.com
ffuz command vary for different request such as requests containing parameters and cookies so from my opinion just brute force directries and use burp suit for another stuff but if you don't know to use burp then see the documentation from above link and hack!!!.

Github Recon
Resources and References Github Dorks https://securitytrails.com/blog/github-dorks GitROB https://michenriksen.com/blog/gitrob-now-in-go/ News https://nakedsecurity.sophos.com/2019/03/25/thousands-of-coders- are-leaving-their-crown-jewels-exposed-on-github/ Github Bug Bounty Hunting https://gist.github.com/EdOverflow/922549f610b258f459b219a32f 92d10b Assetnote https://blog.assetnote.io/bug-bounty/2019/04/23/getting-access- zendesk-gcp/

Automated github recon using GitDorker
see original repo here : GitDorker
see tutorial here : youtube_automated_github_recon_tutorial
google output sheet ably : reconSheetAbly
Steps:
1 clone the repository

git clone https://github.com/obheda12/GitDorker.git
move to GitDorker diretry
cd GitDorker

installation steps
pip3 install -r requirements.txt
use this command for more options
python3 GitDorker.py -h
generate personal access token githubAccount > settings > developer settings > personal access tokens

copy the tokens to a file say github_token_for_gitdoreker.txt

just run command

python3 GitDorker.py -q <give primary query here - say tesla.com> -tf github_token_for_gitdorker.txt -d dorks_file.txt -o output.csv
