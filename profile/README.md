# Coanda Github Home

Welcome to Coanda's Github organization. Here you will find helpful information on interacting with our Github repositories and contributing code.

## Teams

<p align="center">
<a href="https://github.com/orgs/CRD-Coanda/teams/projects">projects</a> |
<a href="https://github.com/orgs/CRD-Coanda/teams/scientific">scientific</a> |
<a href="https://github.com/orgs/CRD-Coanda/teams/cfd">cfd</a> |
<a href="https://github.com/orgs/CRD-Coanda/teams/instruments">instruments</a> |
<a href="https://github.com/orgs/CRD-Coanda/teams/pydaq">pydaq</a>  |
<a href="https://github.com/orgs/CRD-Coanda/teams/dactl">dactl</a>
</p>

## Github Account

Follow the relevant instructions below to set up your GitHub account. Note that there is an annual cost for GitHub of around $180/year so if you are unsure if you actually need an account please discuss with your manager. Please keep anything work related under the Coanda org and not just as part of your personal account.

__If you do not have a GitHub account__
1. Go to github.com and create an account using the sign up button.
1. Use your tetratech.com email address (not your Coanda one).
1. Choose a username that will be recognizable to your colleagues. You could use something like your full name or the 5-character code like "swebs". You could use a prefix like "crd-" if the username you want is not available.
1. Change your display "name" to your full name in the user settings (public profile section).
1. Send an email or Teams chat with your username to Scott Webster or Tom Depew and we will invite your account to the Coanda organization.
1. You will be required to enable 2FA. This is separate from the usual Tetra Tech process, but you can use the same Microsoft Authenticator app. Follow the instructions for setup.
1. Submit an IT helpdesk request for a "GitHub Enterprise Standalone" license (Helpdesk - Software/Applications - Request Software Install/Purchase). Your supervisor will be asked to approve. Let them know about the request and tell them to reach out to Scott Webster or Tom Depew if they have any questions.

__If you already have a GitHub account__
1. Decide if you will use your existing account for work or if you want to create a new account.
1. If you want to create a new account, follow the instructions above.
1. If you want to use your existing account, continue with this section.
    1. Add your tetratech.com email address as an email in your account settings (Emails section).
    1. Make your tetratech.com address your primary address (selection on the same page).
    1. Follow steps 2 to 5 from the new account section above.


## Post-Migration Guide

This section provides instructions for how to point your old "local" repositories to the new remote endpoints at Github.com.

### Authentication

#### ssh key
If you are going to be using ssh-keys, refer to the instructions here:
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh

TODO: maybe we can do a simpler subset of these, need to test on Windows.

#### https

If you want to authenticate with https, it should "just work". When you need to authenticate (i.e. during a clone/pull/push) you will be prompted for a Tetratech Single-Sign-On (SSO) credential. This is the credentials for your CRD-Coanda joined Github account. More information about authentication including https can be found here:
- https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github

### Redirecting

To set the new remote, the command depends on whether you will use ssh or https. In both cases the <repository-name> must be replaced by the name of the repo on GitHub. __YOU WILL NEED TO REFER TO THE REPOSITORY NAME SHEET TO FIND THE MAPPED REPOSITORY NAME__.  The spreadsheet is located [here].

1. Navigate to the local directory containing your git repository.
1. Change the remote url with one of the following commands (depending on your desired authentication mode):

   SSH:
   ```sh
   git remote set-url origin git@github.com:CRD-Coanda/<repository-name>.git
   ```

   HTTPS:
   ```sh
   git remote set-url origin https://github.com/CRD-Coanda/<repository-name>.git
   ```


