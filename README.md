# Ricardian-Contracts
Test repo for Immutable Ecosystem Ricardian Contracts. A private repo of a sample license agreement with branches for each completed agreement form.

# To use
Share the form PDF (website or email). User fills out the PDF form, optionally signs (eSignature or otherwise) and returns it. Upon reciept of completed form, ImmutableSoft branches this repo (using name as repo is private) and commits the changes (completed document) to the branch. Now the GitHub project contains the original PDF in master branch, and minted Ricardian client NFTs in other branches. This works for any type of document, not just PDFs. Document collections and supplements can also be supported in the same manner using ZIP files - best practice is fixed filenames in master ZIP that match client ZIP - empty files in master ZIP for entirely user supplied material (photo of ID, etc.).

In the Dapp (https://ecosystem.immutablesoft.org/)
1. Create a product for this contract agreement.
2. Press New Release button on product management interface and choose a URL (public preferred so applicants can download) for the master PDF file (website, etc.). Include/Compute hash of master PDF file and give it a major and submajor version only (ex. 1.0), leave Ricardian root field empty. Submit release, approve metamask transaction to write release to the blockchain.
  a.If proceeding directly to step 3 below, wait for the transaction above to be confirmed and then refresh the browser page before continuing.
3. When recording client agreements, choose the master PDF version as the Ricardian root, add a minor and subminor version, compute hash. If there are no versions in the Ricardian root dropdown list, perform step 2a above and try again.
