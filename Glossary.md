## Glossary

**Address Space Layout Randomisation (ASLR)** A technique employed by operating  
systems to make the successful exploitation by a software bug much more difficult. By  
ensuring memory addresses and offsets are unpredictable, exploit code can’t hard-code  
these values.

**AES (Advanced Encryption Standard)** A popular global encryption standard used to  
encrypt data to keep it private.

**AES cryptographic engine** A dedicated hardware component that implements AES.

**AES-XTS** A mode of AES defined in IEEE 1619-2007 meant to work for encrypting storage  
media.

**APFS (Apple File System)** The default file system for iOS, iPadOS, tvOS, watchOS and  
Mac computers using macOS 10.13 or later. APFS features strong encryption, space  
sharing, snapshots, fast directory sizing and improved file system fundamentals.

**Apple Business Manager** A simple, web-based portal for IT administrators that provides  
a fast, streamlined way for organisations to deploy Apple devices they have purchased  
directly from Apple or from a participating Apple Authorised Reseller or network provider.  
They can automatically enrol devices in their mobile device management (MDM) solution  
without having to physically touch or prepare the devices before users get them.

**Apple IDentity Service (IDS)** Apple’s directory of iMessage public keys, APNs addresses,  
and phone numbers and email addresses that are used to look up the keys and device  
addresses.

**Apple Push Notification service (APNs)** A worldwide service provided by Apple that  
delivers push notifications to Apple devices.

**Apple School Manager** A simple, web-based portal for IT administrators that provides  
a fast, streamlined way for organisations to deploy Apple devices they have purchased  
directly from Apple or from a participating Apple Authorised Reseller or network provider.  
They can automatically enrol devices in their mobile device management (MDM) solution  
without having to physically touch or prepare the devices before users get them.

**Apple Security Bounty** A reward given by Apple to researchers who report a vulnerability  
that affects the latest shipping operating systems and, where relevant, the latest hardware.

**Boot Camp** A Mac utility that supports the installation of Microsoft Windows on supported  
Mac computers.

**Boot Progress Register (BPR)** A set of system on chip (SoC) hardware flags that software  
can use to track the boot modes the device has entered, such as Device Firmware Update  
(DFU) mode and Recovery mode. After a Boot Progress Register flag is set, it can’t be  
cleared. This allows later software to get a trusted indicator of the state of the system.

**Boot ROM** The very first code executed by a device’s processor when it first boots. As an  
integral part of the processor, it can’t be altered by either Apple or an attacker.

**CKRecord** A dictionary of key-value pairs that contain data saved to or fetched from  
CloudKit.

**Data Protection** A file and keychain protection mechanism for supported Apple devices.  
It can also refer to the APIs that apps use to protect files and keychain items.

**Data Vault** A mechanism — enforced by the kernel — to protect against unauthorised  
access to data regardless of whether the requesting app is itself sandboxed.

**Device Firmware Upgrade (DFU) mode** A mode in which a device’s Boot ROM code waits  
to be recovered via USB. The screen is black when in DFU mode, but upon connecting to  
a computer using iTunes or the Finder, the following prompt is presented: “iTunes (or the  
Finder) has detected an (iPad, iPhone or iPod touch) in Recovery mode. The user must  
restore this (iPad, iPhone or iPod touch) before it can be used with iTunes (or the Finder).”

**direct memory access (DMA)** A feature that allows hardware subsystems to access main  
memory directly, bypassing the CPU.

**Effaceable Storage** A dedicated area of NAND storage, used to store cryptographic keys,  
that can be addressed directly and wiped securely. While it doesn’t provide protection if an  
attacker has physical possession of a device, keys held in Effaceable Storage can be used  
as part of a key hierarchy to facilitate fast wipe and forward security.

**Elliptic Curve Diffie-Hellman Exchange Ephemeral (ECDHE)** A key exchange mechanism  
based on elliptic curves. ECDHE allows two parties to agree on a secret key in a way  
that prevents the key from being discovered by an eavesdropper watching the messages  
between the two parties.

**Elliptic Curve Digital Signature Algorithm (ECDSA)** A digital signature algorithm based on  
elliptic curve cryptography.

**Enhanced Serial Peripheral Interface (eSPI)** An all-in-one bus designed for synchronous  
serial communication.

**Exclusive Chip Identification (ECID)** A 64-bit identifier that’s unique to the processor  
in each iOS and iPadOS device. When a call is answered on one device, the ringing of  
nearby iCloud-paired devices is terminated by briefly advertising through Bluetooth Low  
Energy (BLE) 4.0. The advertising bytes are encrypted using the same method as Handoff  
advertisements. Used as part of the personalisation process, it’s not considered a secret.

**file system key** The key that encrypts each file’s metadata, including its class key. This is  
kept in Effaceable Storage to facilitate fast wipe rather than confidentiality.

**Gatekeeper** In macOS, a technology designed to help ensure that only trusted software  
runs on a user’s Mac.

**group ID (GID)** Like the UID but common to every processor in a class.

**hardware security module (HSM)** A specialised tamper-resistant computer that  
safeguards and manages digital keys.

**HMAC** A hash-based message authentication code based on a cryptographic hash function.

**iBoot** The stage 2 boot loader for all Apple devices. Code that loads XNU as part of the  
secure boot chain. Depending on the system on chip (SoC) generation, iBoot may be  
loaded by the Low Level Bootloader or directly by the Boot ROM.

**Input/Output Memory Management Unit (IOMMU)** An input/output memory management  
unit. A subsystem in an integrated chip that controls access to address space from other  
input/output devices and peripherals.

**integrated circuit (IC)** Also known as a _microchip_.

**Joint Test Action Group (JTAG)** A standard hardware debugging tool used by  
programmers and circuit developers.

**key wrapping** Encrypting one key with another. iOS and iPadOS use NIST AES key  
wrapping, in accordance with RFC 3394.

**keybag** A data structure used to store a collection of class keys. Each type (user, device,  
system, backup, escrow or iCloud Backup) has the same format.

A header containing: Version (set to four in iOS 12 or later), Type (system, backup, escrow  
or iCloud Backup), Keybag UUID, an HMAC, if the keybag is signed, and the method used  
for wrapping the class keys — tangling with the UID or PBKDF2, along with the salt and  
iteration count.

A list of class keys: Key UUID, Class (which file or Keychain Data Protection class),  
wrapping type (UID-derived key only; UID-derived key and passcode-derived key),  
wrapped class key and a public key for asymmetric classes.

**keychain** The infrastructure and a set of APIs used by Apple operating systems and third-  
party apps to store and retrieve passwords, keys and other sensitive credentials.

**Low Level Bootloader (LLB)** On Mac computers with a two-stage boot architecture, LLB  
contains the code that’s invoked by the Boot ROM, and that in turn loads iBoot as part of  
the secure boot chain.

**media key** Part of the encryption key hierarchy that helps provide for a secure and  
instant wipe. In iOS, iPadOS, tvOS and watchOS, the media key wraps the metadata on the  
data volume (and thus without it access to all per-file keys is impossible, rendering files  
protected with Data Protection inaccessible). In macOS, the media key wraps the keying  
material, all metadata and data on the FileVault protected volume. In either case, wipe of  
the media key renders encrypted data inaccessible.

**memory controller** The subsystem in a system on chip that controls the interface between  
the system on chip and its main memory.

**mobile device management (MDM)** A service that lets an administrator remotely manage  
enrolled devices. After a device is enrolled, the administrator can use the MDM service  
over the network to configure settings and perform other tasks on the device without user  
interaction.

**NAND** Non-volatile flash memory.

**nonce** A unique one-off number used in various security protocols.

**Passcode-derived key (PDK)** The encryption key derived from the entangling of the user  
password with the long-term SKP key and the UID of the Secure Enclave.

**per-file key** The key used by Data Protection to encrypt a file on the file system. The per-  
file key is wrapped by a class key and is stored in the file’s metadata.

**provisioning profile** A property list (.plist file) signed by Apple that contains a set of  
entities and entitlements allowing apps to be installed and tested on an iOS or iPadOS  
device. A development provisioning profile lists the devices that a developer has chosen  
for ad hoc distribution, and a distribution provisioning profile contains the app ID of an  
enterprise-developed app.

**Recovery mode** A mode used to restore many Apple devices if it doesn’t recognise the  
user’s device so the user can reinstall the operating system.

**ridge flow angle mapping** A mathematical representation of the direction and width of the  
ridges extracted from a portion of a fingerprint.

**Sealed Key Protection (SKP)** A technology in Data Protection that protects, or _seals_ ,  
encryption keys with measurements of system software and keys available only in hardware  
(such as the UID of the Secure Enclave).

**Secure Storage Component** A chip designed with immutable RO code, a hardware random  
number generator, cryptography engines and physical tamper detection. On supported  
devices, the Secure Enclave is paired with a Secure Storage Component for anti-replay  
nonce storage. To read and update nonces, the Secure Enclave and storage chip employ  
a secure protocol that helps ensure exclusive access to the nonces. There are multiple  
generations of this technology with differing security guarantees.

**sepOS** The Secure Enclave firmware, based on an Apple-customised version of the L4  
microkernel.

**software seed bits** Dedicated bits in the Secure Enclave AES Engine that get appended to  
the UID when generating keys from the UID. Each software seed bit has a corresponding  
lock bit. The Secure Enclave Boot ROM and operating system can independently change  
the value of each software seed bit as long as the corresponding lock bit hasn’t been set.  
After the lock bit is set, neither the software seed bit nor the lock bit can be modified. The  
software seed bits and their locks are reset when the Secure Enclave reboots.

**SSD controller** A hardware subsystem that manages the storage media (solid-state drive).

**System Coprocessor Integrity Protection (SCIP)** A mechanism Apple uses designed to  
prevent modification of coprocessor firmware.

**system on chip (SoC)** An integrated circuit (IC) that incorporates multiple components  
into a single chip. The Application Processor, the Secure Enclave and other coprocessors  
are components of the SoC.

**system software authorisation** A process that combines cryptographic keys built  
into hardware with an online service to check that only legitimate software from Apple,  
appropriate to supported devices, is supplied and installed at upgrade time.

**tangling** The process by which a user’s passcode is turned into a cryptographic key and  
strengthened with the device’s UID. This process helps ensure that a brute-force attack  
must be performed on a given device, and thus is rate limited and can’t be performed in  
parallel. The tangling algorithm is PBKDF2, which uses AES keyed with the device UID as  
the pseudo-random function (PRF) for each iteration.

**Unified Extensible Firmware Interface (UEFi) firmware** A replacement technology for  
BIOS to connect firmware to a computer’s operating system.

**Uniform Resource Identifier (URI)** A string of characters that identifies a web-based  
resource.

**unique ID (UID)** A 256-bit AES key that’s burned into each processor at manufacture. It  
can’t be read by firmware or software and it’s used only by the processor’s hardware AES  
Engine. To obtain the actual key, an attacker would have to mount a highly sophisticated  
and expensive physical attack against the processor’s silicon. The UID isn’t related to any  
other identifier on the device including, but not limited to, the UDID.

**xART** An abbreviation for eXtended Anti-Replay Technology. A set of services that provide  
encrypted, authenticated persistent storage for the Secure Enclave with anti-replay  
capabilities based on the physical storage architecture. See Secure Storage Component.

**XNU** The kernel at the heart of the Apple operating systems. It’s assumed to be trusted,  
and it enforces security measures such as code signing, sandboxing, entitlement checking  
and Address Space Layout Randomisation (ASLR).

**XProtect** In macOS, an antivirus technology for the signature-based detection and  
removal of malware.
