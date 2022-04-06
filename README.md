# Ricardian-Contracts
Example repo for Immutable Ecosystem Ricardian Contracts. Designed to be a private repo used to maintain the completed contracts received by a contract application owner (Contract Service Provider or otherwise). Replace the example PDF of the Immutable Ecosystem Creator agreement with your own agreement within your own private repo. The goal is to utilize GitHub to manage storing client agreements as branches for each completed agreement form. This guide assumes you are somewhat familiar with Git commands and GitHub.com.

# To use GitHub for version and client signed agreement management
1. Share the form PDF (website, email, etc.).
2. Entity representative fills out the PDF form, optionally signs (eSignature or otherwise) and returns it.
3. Upon reciept of completed form, the repo owner branches the repo (GitHub.com UI), naming the branch after signor/entity.
4. Contract owner then clones the repo (if not already), fetch's and checkout's the new branch ('git fetch' and then 'git checkout <branchName>')
5. Once the local repo is in the new branch, replaces the empty PDF with the user completed PDF (same filename) and then commit the changes to the branch ('git commit' and 'git push origin <branchName>').

Now the GitHub project contains the original PDF in master branch, and client agreemnts in other branches named after the client. See the 'SeanLawless' branch in this repo for an example. This works for any type of document, not just PDFs. Document collections and supplements can also be supported in the same manner using ZIP files - best practice is fixed filenames in master ZIP that match client ZIP - empty files in master ZIP for entirely user supplied material (photo of ID, etc.).

# Further secure/tokenize the agreement with an NFT using our Dapp (https://ecosystem.immutablesoft.org/)
1. Create a product for this contract agreement.
2. Press New Release button on product management interface and choose a URL (public preferred so applicants can download) for the master PDF file (website, etc.). Include/Compute hash of master PDF file and give it a major and submajor version only (ex. 1.0), leave Ricardian root field empty. Submit release, approve metamask transaction to write release to the blockchain.

  a.If proceeding directly to step 3 below, wait for the transaction above to be confirmed and then refresh the browser page before continuing.

3. When recording client agreements, choose the master PDF version as the Ricardian root, add a minor and subminor version, compute hash. If there are no versions in the Ricardian root dropdown list, perform step 2a above and try again.
