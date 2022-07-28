<div id="top"></div>


<!-- PROJECT SHIELDS -->
<div align="center">

[![Last Commit][commits-shield]][commits-url]
[![Twitter][twitter-shield]][twitter-url]

</div>



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/DELVES/Warrant-Canaries">
    <img src="https://i.imgur.com/MY7vJ33.png" alt="Logo" width="250" height="250">
  </a>

<h3 align="center">DMG Warrant Canaries</h3>

  <p align="center">
    Warrant canaries applicable to all DELVES Media Group organisations.
    <br />
    <a href="https://delvesmedia.group/"><strong>Learn more about us »</strong></a>
    <br />
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
     <li><a href="#about">About</a></li>
     <li><a href="#what-are-warrant-canaries">What are warrant canaries?</a></li>
    <li>
      <a href="#can-i-verify-a-canarys-authenticity">Can I verify a canary's authenticity?</a>
      <ul>
        <li><a href="#how-to">How to verify</a></li>
      </ul>
    </li>
    <li><a href="what-should-i-do-if-the-warrant-canary-itself-or-parts-of-it-are-missing-for-the-current-period">What should I do if the canary is missing?</a></li>
    <li><a href="#current-signers">Current signers</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT -->
## About

Many journalists worldwide have been subject to subpoenas to hand over information about their sources, combined with gag orders making it illegal to tell anyone that they have received such requests. These unlawful and unconstitutional legal processes infringe on the freedom of the press.

As a trusted source for information on current events, DELVES Media Group is committed to protecting its sources and audiences. We're launching the use of warrant canaries to inform our audiences about potential interferences in our work by government agencies and non-state actors. Our warrant canary helps our audiences whether we are under duress, have received a press super-injunction, DSMA notice/letter, subpoena, warrant or other legal compulsions that we would be prohibited from disclosing. If our company is subject to such a legal process, relevant notices in our warrant canary will disappear.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- WHAT ARE WARRANT CANARIES -->
## What are warrant canaries?

> A warrant canary is a colloquial term for a regularly published statement that a service provider has not received legal process that it would be prohibited from saying it had received. Once a service provider does receive legal process, the speech prohibition goes into place, and the canary statement is removed.
>
> Warrant canaries are often provided in conjunction with a transparency report, listing the process the service provider can publicly say it received over the course of a particular time period. The canary is a reference to the canaries used to provide warnings in coalmines, which would become sick before miners from carbon monoxide poisoning, warning of the danger.

~ [Electronic Frontier Foundation](https://www.eff.org/deeplinks/2014/04/warrant-canary-faq)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- WHAT SHOULD I DO IF THE CANARY IS MISSING -->
## What should I do if the warrant canary itself or parts of it are missing for the current period?

If there is no warrant canary published at the designated dates or if parts of the canary appear to be removed, **take caution** when communicating with us or viewing our work. When under duress due to censorship tactics like gag orders, it may be impossible for us to communicate with our audiences or sources about what is going on. We encourage people that have noticed these anomalies to spread the word on social media platforms to give ourselves a voice when we can't speak.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CAN I VERIFY A CANARYS AUTHENTICITY -->
## Can I verify a canary's authenticity?

Yes! It's essential to verify a canary's authenticity to assess whether it was written by those who claim to have written it. All of our warrant canaries are PGP signed with the signatures in cleartext on the canary file.

### How-to

To verify the signature of a canary, you'll need to install a package and complete a few simple steps. We recommend using [Homebrew] to install the required package.
* [gnupg]
  ```sh
  brew install gnupg
  ```

Once gnupg is installed on your device, you'll need to import the public keys of all signers. Their fingerprints can be found [here](#current-signers).
Copy each fingerprint and run this command, replacing ADDFINGERPRINTHERE with the real fingerprint:
  ```sh
  gpg --search-keys "ADDFINGERPRINTHERE"
  ```

You should get a result that looks something like this:
  ```sh
gpg: data source: https://keys.openpgp.org:443
(1)	Rick Astley <nevergonna@giveyou.up>
	  256 bit EDDSA key ABCDEFGHIJKLMNOP, created: 2020-04-01
Keys 1-1 of 1 for "1234 5678 9012 3456 7890 1234 ABCD EFGH IJKL MNOP".  Enter number(s), N)ext, or Q)uit > 
  ```

You can see that the 1st result matches with one of our current signers so type `1` and hit enter to import the public key.

Now that the key has been imported, you can now download the warrant canary from our repository.
Once it has been dowmloaded, run the following command, replacing the file path with the actual path where the canary is stored on your device:
  ```sh
  gpg --verify /users/rickastley/Downloads/test.txt
  ```

  If you recieve an output like this saying that there is a 'good signature', you have sucessfully verified that the canary is authentic.
  ```sh
  gpg: Signature made Tue 15 Mar 17:32:23 2022 GMT
gpg:                using EDDSA key 123456789012345678901234ABCDEFGHIJKLMNOP
gpg: Good signature from "Rick Astley <nevergonna@giveyou.up>" [ultimate]
```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CURRENT SIGNERS -->
## Current Signers

[**Hamzah Batha**](https://keybase.io/hamzahbatha) | C37F 68EA 48E1 5168 8AB1 192B A7D6 B1CC 0A01 AD4C

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments
DMG's use of warrant canaries is part of an initiative supported by a coalition of nonprofits and institutions (listed below). The aim is for companies, organisations and service providers to publish warrant canaries to aid in the fight against illegal and unconstitutional national security processes, including National Security Letters and other secret court processes.

* [Electronic Frontier Foundation](https://www.eff.org/)
* [Freedom of the Press Foundation](https://freedom.press/)
* [New York University School of Law](https://www.law.nyu.edu/)
* [The Calyx Institute](https://calyxinstitute.org/)
* [The Berkman Klein Center for Internet & Society](https://cyber.harvard.edu/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[commits-shield]: https://img.shields.io/github/last-commit/DELVES/Warrant-Canaries?style=for-the-badge
[commits-url]: https://github.com/DELVES/CanaryWriter/commits
[twitter-shield]: https://img.shields.io/twitter/follow/DELVEScanaries?color=CEFF00&style=for-the-badge
[twitter-url]: https://twitter.com/DELVEScanaries
[Homebrew]: https://brew.sh/
[gnupg]: https://gnupg.org/
