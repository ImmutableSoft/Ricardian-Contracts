# Ricardian-Contracts

A Ricardian contract is any human readable and agreeable document, such as a form, signed contract, application, etc. This repository is an example for how a Git repository can be used to manage client contracts and integrate with creating Ricardian Contracts enforcable within the Immutable Ecosystem. While this example is public, a private repo should be used in production to maintain the completed contracts received from users. Replace the example PDF of the Immutable Ecosystem Creator agreement with your use case/agreemnt and within your own private Git repository. The innovation is to utilize GitHub to privately manage storing client agreements as branches for each completed agreement form. 

With file and access management handled by GitHub, it is possible to create NFTs that are linked as signatories to the public master contract PDF. Ownership of these NFTs may grant rights as defined in the Ricardian contract and enforced by Immutable Ecosystem and other smart contracts. This guide assumes you are somewhat familiar with Git commands and have a GitHub.com account. It also you assumes you are familiar with how ImmutableSoft bridges Ricardian contracts into smart contracts as defined in our [Better Programming article Ricardian Contract Interoperability](https://betterprogramming.pub/ricardian-contract-interoperability-9b9e2919dc43?source=friends_link&sk=941a297dcf0c99561d359b4f2c713f4f).

# Use GitHub for client signed PDF agreement management

## Initial setup for master PDF/ZIP

Create a private repo on GitHub named after the type/name of contract or similar. Add a single file that is the master PDF form document of the contract. OR, multiple master/blank PDF form document(s) and/or blank supplemental information files (photo of ID, etc.). Once satisfied, commit and push the PDF file(s) to the main branch of the repository. You can always make a new version of the file(s) later.

Create a release for the repository using only major and submajor versioning. If using multiple PDF forms/supplemental files then this release ZIP file (download from GitHub) is considered the on-boarding material. If only a single PDF, that PDF (not the release ZIP) is considered the on-boarding docuemnt and this release is purely to track versioning. Online/web forms can also be designed to generate a PDF and can be used in leui of an actual PDF sent to and filled out by the user/client. This is outside the scope of this discussion but storing the resulting autogenerated client PDF file on GitHub can be automated.

For new versions of the master contract PDF, update the PDF file and push the change to the 'main' branch. Then create a new release with incremented version (steps 2, 3, 4, 5). Use this new version for future client acquisition and update Immutable Ecosystem as applicable.

## Use Git repository to archive a client agreement

Share the form PDF (website, email, social media, Immutable Ecosystem, etc.). Once an entity representative/user fills out the PDF form (optionally signs with eSignature, scanned copy, sign field, etc.) and returns it, the Git repository owner branches the repository (using GitHub.com UI), naming the branch after the new signor/entity. In Git parlace, the contract repo owner clones the repo (if not already), fetch's and checkout's the new branch ('git fetch' and then 'git checkout {branchName}'). Once the new branch is active, the owner replaces the empty PDF in that directory with the user completed PDF (same filename). Then the repo owner commits the changes to the client branch ('git commit' and 'git push origin {branchName}').

If that sounds complicated, don't worry, this can all be acheived using GitHub's advanced web UI. To summarize we want to create a new branch, replace the file and then commit/pushing the change to the new branch. To create a new branch, press the small Main dropdown list in top left of the GitHub repository main page (just above the first file). Type in the new branch name (client name, etc.) and select Create branch ... from 'main' to create and move the Git web UI to this new branch. The small Main dropdown in the top left should then change to the name of the new branch, indicating the current branch.

![image branch-drop](./images/branch-dropdown.png)

Once in the new branch, click the Add Files drop down and Upload files. Then drag and drop the client PDF to your browser page of the GitHub repository opened to the new branch. It will then open a Commit request page where you can give the commit some additional information (sales associate's name, etc.) before Commiting the change to this new branch.

![image branch-commit](./images/branch-commit.png)

Now the GitHub repository contains the original PDF in 'main' branch, and client agreemnts in other branches named after the clients. See the 'SeanLawless' branch in this repo for an example. There are no limits on the number of branches and this works for any type of document or file, not just PDFs. Document collections and supplements are best supported in the same manner using ZIP files - best practice is fixed filenames in master ZIP that match client ZIP - empty files in master ZIP for entirely user supplied material (photo of ID, etc.).

# Tokenize contract within NFT using [Immutable Ecosystem Dapp](https://ecosystem.immutablesoft.org/)

## Initial setup 

Create a product for this contract agreement in the Immutable Ecosystem. Each different master contract PDF/ZIP must be a different product. See the [Immutable Ecosystem Documentation](https://immutablesoft.github.io/ImmutableEcosystem/#the-product-and-release-interfaces) for more information on registering and creating a product.

Navigate to your Product in the Dapp and press the New Release button. In the resulting form, paste a URL (public preferred so applicants can download directly) for the master/main PDF file (website, etc.). Remember your Git repo is private so you should not use that URL here. Include/Compute hash of master PDF/ZIP file and give it a major and submajor version only (ex. 1.0) that matches your GitHub release version. Leave Ricardian root field empty. Submit release, approve metamask transaction to submit new release to the blockchain and wait for the transaction to be mined.

If proceeding directly to Recording a client PDF below, wait for the transaction above to be confirmed and then refresh the browser page before continuing.

New versions of the master contract PDF should be recorded as above, using incrementing/increasing major and/or submajor version numbers and matching the major versioning used in GitHub. Client PDF versions should have the corect master version selected as their Ricardian root during creation (see below).

## Recording a client PDF

When recording client agreements, choose the correct master PDF version as the Ricardian root, add a minor and/or subminor version, and compute hash of client PDF/ZIP. If there are no versions in the Ricardian root dropdown list, try refreshing the Dapp page in your browser.

Client PDF versions must adhere/match the selected Ricardian root master PDF version. Please select correct version of the Ricardian root during creation. The default is the most recent version.

## Verify a master or client PDF

To verify a PDF/ZIP release just drag and drop the file to the Authenticate bar at the top of the [Immutable Ecosystem Dapp](https://ecosystem.immutablesoft.org/). See our [Drag and drop authenticate demo](https://youtu.be/Yd703JdM-xg) on YouTube for more information.

