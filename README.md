# Operating System Update Pipeline Using GitHub Actions or GitLab CI/CD

This guide outlines the process to set up and execute Operating System updates using either GitHub Actions or GitLab CI/CD.

# GitHub Actions

`.github` is useful if you are planning to run a pipeline on GitHub and implement the GitOps approach.

Remove the `.example` part from the name of the files in `.github/workflow` for the GitHub Actions pipeline to work.

You can delete `.github` if you are not planning to use the GitHub pipeline.

## Run the OS Update Workflow Using GitHub Actions

1. Ensure you have the required secrets (`SSH_USER`, `EC2_HOST`, and `SSH_PRIVATE_KEY`) set up in your repository's Secrets settings.
2. Ensure the EC2 instance's security group allows incoming SSH connections from the GitHub Actions runner IP addresses.
3. Make sure the SSH user has the necessary permissions on the EC2 instance, including `sudo` permissions if required.

### Steps:

1. **Navigate to the GitHub Repository**: Go to your repository where the workflow is set up.

2. **Go to the 'Actions' Tab**: Located at the top of your repository.

3. **Select the 'Application Update' Workflow**: You should see this on the left sidebar. Click on it.

4. **Run Workflow**: Towards the right side, you'll see a "Run workflow" dropdown. Click on it.

5. **Provide Input (Optional)**:
    - You can provide a reason for the run in the "Reason for run" input box. This is optional.

6. **Click 'Run workflow' Button**: After clicking, the workflow will start, and you can observe its progress.

7. **Check the Results**: Once the workflow completes, you can click on the specific job to view the logs and see if the OS update was successful on your EC2 instance.

# GitLab CI/CD

`.gitlab-ci.yml` is useful if you are planning to run a pipeline on GitLab and implement the GitOps approach.

Remove the `.example` part from the name of the files in the root or designated CI/CD directory to make the GitLab CI/CD pipeline operational.

You can delete `.gitlab-ci.yml` if you are not planning to use the GitLab pipeline.

## Run the OS Update Workflow Using GitLab CI/CD

1. Ensure you have the required CI/CD variables (`SSH_USER`, `EC2_HOST`, and `SSH_PRIVATE_KEY`) set up in your GitLab project's settings.
2. Ensure the EC2 instance's security group allows incoming SSH connections from the GitLab runner IP addresses.
3. Make sure the SSH user has `sudo` permissions on the EC2 instance to run update commands.

### Steps:

1. **Navigate to the GitLab Project**: Go to your project where the `.gitlab-ci.yml` file is set up.
  
2. **Go to the 'CI/CD' Section**: Located in the left sidebar of your project.
  
3. **Select the 'Pipelines' Tab**: Here, you'll see a list of pipelines that have been run or are scheduled to run.
  
4. **Run Pipeline**: At the top-right corner, you'll find the "Run Pipeline" button. Click on it.
  
5. **Choose the 'main' Branch**: As the `os_update` job is set to run only on the `main` branch.
  
6. **Click 'Run Pipeline' Button**: Once you've selected the branch, click the "Run Pipeline" button. This will initiate the OS update job, and you can monitor its progress.
  
7. **Check the Results**: After completion, you can click on the specific job within the pipeline to view the logs and verify if the OS update was successful on your EC2 instance.

# Author

I’m Vladimir Mikhalev, the [Docker Captain](https://www.docker.com/captains/vladimir-mikhalev/), but my friends can call me Valdemar.

🌐 My [website](https://www.heyvaldemar.com/) with detailed IT guides\
🎬 Follow me on [YouTube](https://www.youtube.com/channel/UCf85kQ0u1sYTTTyKVpxrlyQ?sub_confirmation=1)\
🐦 Follow me on [Twitter](https://twitter.com/heyValdemar)\
🎨 Follow me on [Instagram](https://www.instagram.com/heyvaldemar/)\
🧵 Follow me on [Threads](https://www.threads.net/@heyvaldemar)\
🐘 Follow me on [Mastodon](https://mastodon.social/@heyvaldemar)\
🧊 Follow me on [Bluesky](https://bsky.app/profile/heyvaldemar.bsky.social)\
🎸 Follow me on [Facebook](https://www.facebook.com/heyValdemarFB/)\
🎥 Follow me on [TikTok](https://www.tiktok.com/@heyvaldemar)\
💻 Follow me on [LinkedIn](https://www.linkedin.com/in/heyvaldemar/)\
🐈 Follow me on [GitHub](https://github.com/heyvaldemar)

# Communication

👾 Chat with IT pros on [Discord](https://discord.gg/AJQGCCBcqf)\
📧 Reach me at ask@sre.gg

# Give Thanks

💎 Support on [GitHub](https://github.com/sponsors/heyValdemar)\
🏆 Support on [Patreon](https://www.patreon.com/heyValdemar)\
🥤 Support on [BuyMeaCoffee](https://www.buymeacoffee.com/heyValdemar)\
🍪 Support on [Ko-fi](https://ko-fi.com/heyValdemar)\
💖 Support on [PayPal](https://www.paypal.com/paypalme/heyValdemarCOM)
