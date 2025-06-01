# Ideal Reset

Install a system from a configuration folder.

## Notes

- Encryption shouldn't be integral to `ireset-tools`. Instead, use another tool `archivex` to lock the whole ireset-base directory and `cryp` to decrypt it. `Ireset` never knows anything about encryption. Encryption happens at a parent level.

- ircp.local, ircp.s1 are my personal scripts to easy update ireset-install-images. These must be generalized to config file.

## Assisting tools

Just rename the creds file to disable using it. Must have 'creds' and 'creds-wanted' file for the check to be done initially.

Create a directory where you configure your installation and all scripts used to install the target system. This system is an interface for interacting with such a directory for purpose of installing a target system. The directory is made to beself-contained and portable to be used in live environments.

Archivex has is_archivex file to denote its of that kind.

A list of folders to encrypt:
archivex-folders-to-encrypt
archivex-key-and-iter - set key and iter for archivex

## Usage procedure

Ireset usage is devided into:

- pre-configuration,
- composing,
- applicagion.

### Pre-configuration

1. Create a directory where you configure your installation and write all scripts meant to run at the installation procedure to install the target system. These are the highly specific steps unique to your system, like network settings, adding user accounts, configuring graphic drivers, configuring specific software, importing your dot-files library etc.

Create the cred file.

## Folder structure

Ireset is devided into:

- system space,
- user space.

### System space

Ireset abstracts away common functionality to build, preform checks, and run installation scripts. Purpose is to not have to concern yourself with this.

### User space

All configuration is done in the user space. This is where you configure the installation for a particular target system to your liking.

Variables available in user space:

User space scripts in options, checks, and install-steps all recieve $BASE_DIR as $1, meaning the instalation-config directory.

## Creating a folder structure

The `ireset-tools` work with a specific folder structure. It is as follows.
