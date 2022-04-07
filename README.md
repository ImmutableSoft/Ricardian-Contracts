# Ricardian-Contracts

Example for using Immutable Ecosystem Ricardian Contracts. A Ricardian contract is any human readable and agreeable document, such as a form, signed contract, application, etc. Designed to be a private repo used to maintain the completed contracts received by a contract application owner (Contract Service Provider or otherwise). Replace the example PDF of the Immutable Ecosystem Creator agreement with your own agreement within your own private repo. The goal is to utilize GitHub to privately manage storing client agreements as branches for each completed agreement form. 

With file and access management on GitHub, it is now possible to create NFTs that are linked as signatories to the public master contract PDF. Ownership of these NFTs may grant rights as defined in the Ricardian contract and enforced by Immutable Ecosystem and other smart contracts. This guide assumes you are somewhat familiar with Git commands and have a GitHub.com account.

# Use GitHub for client signed PDF agreement management

## Initial setup for master PDF/ZIP

1. Create a private repo on GitHub named after the type/name of contract or similar
2. Add a single file that is the master PDF form document of the contract. OR, multiple master/blank PDF form document(s) and/or blank supplemental information files (photo of ID, etc.).
3. Commit and push the PDF file(s) to the main branch of the repository.
4. Create a release for repository using only major and submajor versioning. If multiple PDF forms/supplemental files the release ZIP file is your on-boarding packet. If only a single PDF, that PDF (not the release ZIP) is the on-boarding packet. Online/web forms can also be designed to generate a PDF and can be used in leui of an actual PDF sent to and filled out by the user/client.
5. For new versions of the master contract PDF, update the PDF file and push to 'main' branch. Create a release with new version (steps 2, 3, 4, 5) and use new version for future client acquisition. 

## Use Git repository to archive a client agreement

1. Share the form PDF (website, email, social media, etc.).
2. Entity representative fills out the PDF form, optionally signs (eSignature or otherwise) and returns it.
3. Upon reciept of completed form, the repo owner branches the repo (using GitHub.com UI), naming the branch after the signor/entity.
4. Contract owner then clones the repo (if not already), fetch's and checkout's the new branch ('git fetch' and then 'git checkout {branchName}')
5. Once the local repo is in the new branch, the owner replaces the empty PDF in that directory with the user completed PDF (same filename).
6. Then the repo owner commits the changes to the client branch ('git commit' and 'git push origin {branchName}').

Now the GitHub project contains the original PDF in 'main' branch, and client agreemnts in other branches named after the clients. See the 'SeanLawless' branch in this repo for an example. This works for any type of document, not just PDFs. Document collections and supplements can also be supported in the same manner using ZIP files - best practice is fixed filenames in master ZIP that match client ZIP - empty files in master ZIP for entirely user supplied material (photo of ID, etc.).

# Tokenize contract within NFT using [Immutable Ecosystem Dapp](https://ecosystem.immutablesoft.org/)

## Initial setup 

1. Create a product for this contract agreement. Each different master contract PDF must be a different product. See the [Immutable Ecosystem Documentation](https://immutablesoft.github.io/ImmutableEcosystem/#the-product-and-release-interfaces) for more information.
2. Press New Release button on product management interface and choose a URL (public preferred so applicants can download) for the master/main PDF file (website, etc.). Include/Compute hash of master PDF file and give it a major and submajor version only (ex. 1.0), leave Ricardian root field empty. Submit release, approve metamask transaction to write release to the blockchain.
3. If proceeding directly to Recording a client PDF below, wait for the transaction above to be confirmed and then refresh the browser page before continuing.
4. New versions of the master contract PDF should be recorded as in step 2. above, using incrementing/increasing major and/or submajor version numbers. Client versions that adhere to this new version should have that version selected as their Ricardian root during creation.

## Recording a client PDF

1. When recording client agreements, choose the correct master PDF version as the Ricardian root, add a minor and subminor version, compute hash of client PDF/ZIP. If there are no versions in the Ricardian root dropdown list, perform step 3 above and try again.
2. Client PDF versions must adhere/match the selected Ricardian root master PDF version. Please select correct version as the Ricardian root during creation. The default is the most recent version.

## Verify a master or client PDF

1. To verify a PDF/ZIP release just drag and drop the file to the Authenticate bar at the top of the [Immutable Ecosystem Dapp](https://ecosystem.immutablesoft.org/). See our [Drag and drop authenticate demo](https://youtu.be/Yd703JdM-xg) on YouTube for more information.

