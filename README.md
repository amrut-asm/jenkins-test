# jenkins-test
Testing out jenkins without a public ip (using webhook relay)

# Steps

1. Sign up on webhook relay for relaying webhook events from GitHub to our jenkins instance (since we do not have access to a publicly routable IP).
2. Use relay to generate a webhook link and add the webhook link to your github project page.
3. Install GitHub plugin for Jenkins and enable "GitHub hook trigger for GITScm polling" (under Build Triggers).
4. Add commands that Jenkins should execute after cloning the git repository. (under Build Environment)
5. Update any file in the repo and check if Jenkins clones and runs our commands (the ones we asked Jenkins to execute, under Build Environment).
