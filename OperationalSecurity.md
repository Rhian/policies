# Preamble

Intended to be a non-exhaustive approximation of an operational security guide that should allow for both rapid practical application and deeper study over time. Takes as comprehensive an approach to privacy and security as efficiently possible, covering data available to low level threat actors, corporates, high level threat actors, governments. None of the guidance here constitutes legal advice in any way shape or form, nor does it encourage any pursuit beyond that which is legal and necessary for maximizing individual, and through this, organizational security. 

## Key Points  

+ Privacy and Security are encapsulated.
+ Everyone who trusts and shares information with you depends on your ability to keep yourself secure. If you are compromised, so are the systems and the people you have access to. 
+ Understand the process for compromising people and infrastructure from an offensive perspective & remain up to date with new developments and strategies in both. 
+ It's likely that at some point "is this enough" will cross your mind. The only way to really find the answer to this in a *controlled* way is through red teaming. 
+ Let Red Team results guide you - make sure that this happens as needed, or every 6-12 months. 
+ The smaller the attack surface & the less you give your adversaries the better. 

## Prerequisites

+ Understanding of your risk appetite. 
+ Time

## Risk Appetite 

The return on investment from time spent building strong individual privacy and security will vary in accordance with the type of risk you are looking to mitigate. It's assumed that all of the below are likely to be within the scope of interest. 

### Categories

+ Low Level Threat Actors (unfocused, cookie cutter methods)
+ Corporates 
+ High Level Threat Actors (determined, skilled or both)

## Literature

It is generally understood that a practical understanding of computer science, law, the history of digital and human intelligence (and adjacent areas) is beneficial. Here we will explicitly focus on offensive privacy and security areas that should be considered "core" to what we're trying to achieve as per the preamble, with as little fat as possible. 

## Privacy & Security 

Useful references;

+ Michael Bazzel - Open Source Intelligence Techniques.
+ Michael Bazzel - Extreme Privacy
+ Red Team Field Manual.
+ Blue Team Field Manual.
+ Tangled Web.
+ Attacking Network Protocols.

## Standard Cultural Operating Procedures

1. Encrypt your work and personal computers, phones & external secondary storage. 
2. Do not enmesh the security of the organization with your personal security as far as reasonably possible. This includes, in-exhaustively, passwords, password managers, automated backups, cloud storage, thumb drives. 
3. Work communications should be kept to a limited set of pre-approved platforms. Default to matrix, keybase and signal. 
4. If you change your computer/hard-disk, delete all the data on it (zero'd out) and then physically destroy the disk. Do not give it to a friend, your aunt, your dog or anyone else.
5. The terms of the NDA apply and are non-discretionary. Before sharing any information relating to your role, be certain of who you are talking to. Information may be shared where:
    + It is part of your pre-described job (in for example sales or marketing) AND you are working with materials approved by the Executive Office. 
    + The individual works for Januus AND the information they are asking for is relevant for them in the performance of their role.
6. If you're uncertain of who you're talking to, or something doesn't seem right - enumerate them as far as possible and record their characteristics, if possible try to extract ear-markers that will help us retroactively assess the sophistication of the threat actor, examples of these would include:
    + phone number
    + email address
    + physical locations
    + physical attributes
    + legal entities

7. Be aware of the operating culture of family and friends. Segment yourself digitally accordingly. 
8. Assume every external conversation you have is being recorded and may later be used against you. 
9. Don't leave your devices unlocked or lying around anywhere. Never give your phone to a stranger who asks you if he can call his wife!
10. Use 2-factor authentication wherever possible. Avoid SMS. Hardware keys (yubikey) are great. 
11. If you need to do something with a piece of software you certainly would not trust the owner of - run it in a VM. 
12. Do not upload any software written internally by the company to virustotal or any other online virus scanner. 
13. If you need to delegate material access to Januus resources, give the minimum access possible. 
14. Backups - make them. Use local disks wherever possible and avoid cloud services for anything you wouldn't be happy with being subpoena'd or viewed with a search warrant. 
15. If you think there's a direct or immediate risk of your devices falling into the hands of unknown, untrusted, unaccountable actors - destroy them and rely on your backups. 
16. If you're not sure, ask. 

# Privacy/Security Cheatsheet Notes

## Authentication 

### 2FA

+ Authy for general purpose use.
+ Yubikey for secure long term centralized storage. 

### Password Managers

+ Local - KeepassXC
+ Browser - Bitwarden or Lastpass

## Phones

Ideally buy second hand at random. Replace every 6-18 months depending on risk appetite. Apple vs Android an ongoing debate. Apple understood to have better security and privacy by default. In the case of both it's the cloud accounts to worry about - icloud and google accounts. 

Data coming from your cell phone by default:

+ Bluetooth signal. (Geolocates device locally, see "wardriving" for more info)
+ Wireless signal. (Geolocates device locally, similar to bluetooth but yields more versatile information from a tracking perspective (mac addr) & is wired in with ISPs)
+ Cellular data signal. (Geolocates device locally using cellular towers, the same network data given as for a wireless signal)
+ Radio signal - IMEI & SIM Data. 

### IMEI

+ IMEI uniquely identifies each mass manufactured device.
+ IMEI and phone number will be constantly broadcast to cell towers on more or less any commercial cellphone.
+ IMEI and phone broadcasting generally continues - __even when the phone is off__. This is the case with all iphones and many samsung devices. 
+ Location is found using the strength of the signal as it travels to surrounding towers followed by triangulation from there. Accurate to within 100m depeneding on cell tower frequency amongst other factors. In western cities & with modern phones it will be accurate to within 30m. 

#### Cell-siting - Worth a Glance

+ https://developers.google.com/maps/documentation/android-sdk/location#location_permissions
+ https://community.opencellid.org/t/how-to-locate-a-phone-with-only-phone-number-or-imei-number-we-cant/159 (commercial cell-site from mobile connection)

## Phone Numbers 

+ Two ways to obscure a phone number: Number porting and number forwarding.
+ Having secondary sim cards (with or without data) around proves useful for when throwaway SMS is needed. 
+ Virtual numbers that aren't blacklisted can be found here; https://5sim.net/
+ If you need to do something you want extra privacy for - get a new phone (IMEI) and sim (cell number) with cash and dispose of them afterwards. 

## Emails

+ If you buy a domain, be aware of the registration details you're using. For private domains use https://njal.la . 
+ The closer you can get to a 1;1 ratio of unique mail:service the better. With many providers this is not practical but there are a few secure (tutanota) and less secure (icloud) services that allow you to create many aliases cheaply or for free.
+ Secure centralized email accounts OUTSIDE of corporate / work communications should be cleaned once every 1-3 hardware cycles, depending on exposure. 

## Personal Computer Hardware

+ Change every 6-18 months depending on risk appetite. Synchronize your hardware changes with your cloud changes along with anything else that might compromise otherwise "fresh" hardware.
+ First hand okay. If second hand buy randomly. 

## Aliases

+ Change in sync with hardware changes. 
+ Be aware of patterns in your selection of alias names. Someone who knew 3 of your aliases should not be able to pick 2 of your other aliases from a lineup of 10 random names. 

## Physical Addresses

Alternatives to using your own address: 

+ Hotels
+ PO Boxes
+ Private Mail Boxes
+ Known sites

## Operating Systems 

Avoid Windows. Common choices: 

+ Debian variants (Ubuntu)
+ macOS. 

## Browsers

+ Firefox
+ Chromium (un-googled)
+ Brave (built on chromium). 

### Browser Setup

+ Settings adjusted for privacy. 
+ Ad / Script blocker. 
+ Password Manager (Bitwarden or Lastpass).

## Payments

+ Cash
+ Prepaid cards, physically bought - https://www.ixaris.com worth a look. 
+ There's a whole collection of ways you can obscure your crypto. Remember where you're getting it from in the first place though (do they have your ID?) & consider transaction analysis. 
+ Paypal virtual mastercard. 
+ Privacy.com (US residency)
+ Monzo & Revolut have a feature that allows you to generate a new card for a given transaction - a great all round addition from a security and privacy perspective. 
