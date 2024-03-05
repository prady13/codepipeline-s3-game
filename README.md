# Continuous Deployment using AWS Code Pipeline and S3

## TL;DR
Code for a game is hosted in GitHub.  We create an S3 bucket for static website hosting, then create a continuous deployment pipeline (using AWS Code Pipeline) to automatically deploy the code whenever changes are made.

<img width="1161" alt="Screenshot 2024-02-27 at 1 52 15 PM" src="https://github.com/prady13/codepipeline-s3-game/assets/62207613/9cb67fa5-14ec-4337-a658-cd6dc6aaf43f">


## The Game
A simple memory matching game.  The user clicks two cards (images of memes) to try to match them.  If there's a match, the cards disappear from the board.  If there's no match, the cards are flipped back to their blank side so the user can try again.


## The Deployment Environment
The code will be deployed and hosted in S3.

## The Deployment Pipeline
The pipeline is created using AWS Code Pipeline.  The pipeline pulls the code from GitHub, and deploys it to S3 whenever a change is detected in the code.

## Cost
All services used are eligible for the [AWS Free Tier](https://aws.amazon.com/free/).  However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.
