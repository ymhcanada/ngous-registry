# Welcome to the `.ngo.us` Subdomain Registry

![image](https://github.com/user-attachments/assets/fa5569d1-1c39-4b4e-b11e-6cafb4929bbd)

Welcome to the `.ngo.us` subdomain registry, a platform created to support nonprofit organizations and projects around the globe. We recognize that domain registration costs have increased significantly, which can be a challenge for non-commercial entities working to make a positive impact. Our mission is to eliminate this financial barrier by offering free subdomain registration services for organizations that are unaffiliated with governmental bodies and operate on a non-commercial basis.

## Features

### Nonprofit Focused
The `.ngo.us` registry exclusively supports nonprofit, nongovernmental organizations (NGOs) and initiatives.

### Easy Verification
Our verification process is simple and straightforward. We rely on your organization’s existing online presence for quick approval and evidence-based verification.

### Free Renewal, Forever
Once your subdomain is approved, you’ll enjoy the right to use the subdomain for life, with no registration or renewal fees.

### Included in Mozilla PSL
Our domain is part of the [Mozilla Public Suffix List (PSL)](https://publicsuffix.org), which enhances security by ensuring subdomains are treated independently by browsers, much like `.co.uk`. However, please note that `.ngo.us` is **not** an ICANN-accredited TLD. See the disclaimer below for more details.

## Eligibility Requirements

- **Nonprofit Organizations**: Any existing nonprofit organization, project, or initiative is eligible to apply. There is no need to be incorporated or officially registered with a government body.
- **Public Online Presence**: Your organization must have an existing, publicly visible online presence (e.g., a social media profile) that provides sufficient information about your history and activities.
- **Legal and Good Faith**: Your organization must meet the requirements specified in our terms of service, including operating legally and in good faith.

## Application Process

### 1. Star and Fork this Repository
Star and [fork this repository](https://github.com/ngo-us/registry/fork) to begin the application process.

### 2. Edit the `db.ngo.us` Zone File
Follow the formatting example provided to apply for a domain. For instance, if you wish to register the domain `happycat.ngo.us` for a proejct named `Happy Cat Foundation` and the nameservers are `example1.ns.cloudflare.com.` and `example2.ns.cloudflare.com.`, edit the zone file `db.ngo.us` in your forked repository by adding the following block:

```
; Happy Cat Foundation
; Submitted by networking team <happycat@gmail.example.com>
happycat 86400 IN NS example1.ns.cloudflare.com.
happycat 86400 IN NS example2.ns.cloudflare.com.

```

**Key points to comply:**

1. **Two comment lines** are required at the top of your block:
   - The first line should be your organization's full name.
   - The second line should be your organization's contact email (use an organizational or team-based email, not a personal one). Ensure the domain of the email address is **not** the same as the `.ngo.us` domain you're applying for.

2. **Format and order**:
   - Ensure the domain blocks are ordered alphabetically by your organization's name.
   - If you're applying for multiple domains under the same organization, list them alphabetically.

3. **Nameserver (NS) records**:
   - You must include **at least two nameservers (NS)** for each domain.
   - Use a Time to Live (TTL) value of `86400` (24 hours).

After completing the edit, follow the remaining steps to commit, push, and create a pull request as outlined in the PR template. Make sure all entries follow the correct alphabetical order to ensure smooth processing.

### 3. Submit a Pull Request (PR)
Commit and push your changes to your forked repository, then create a pull request (PR) to this repository. 

In the PR body, provide the details about your nonprofit, including verifiable social media links:

- **Intended Use of Domain**: Describe in detail how you plan to use the domain.
- **Organization Online Presence URLs for Verification**: Include URLs to your organization’s public online profiles (e.g., social media accounts) that provide verifiable information about your cause.  
  - Please ensure that the exact domain name you are applying for is mentioned prominently on one of these profiles (e.g., in your bio, a post, or a comment from your organization’s social media profile page). For example, if you are applying for `happycat.ngo.us`, ensure "happycat.ngo.us" is visible on your organization's social media.
- **Sign the Agreement**: Follow the PR template to sign the agreement.

### 4. Monitor Your PR
Once your pull request is submitted, make sure all automatic checks pass. PRs with failing checks will be ignored. Monitor the PR in case there are any requests for changes, such as corrections to syntax errors in your zone file.

After the PR is reviewed and merged, please allow up to 48 hours for the changes to propagate.

## Modify Existing Registry Records

If you need to update or modify the DNS records of your existing `.ngo.us` domain, follow the steps below:

1. **Fork the Repository**: 
   Use the same GitHub account you initially used to register your domain. Fork this repository if you haven't already, or pull the latest changes from the main repo into your existing fork.

2. **Edit the `db.ngo.us` Zone File**:
   In your forked repository, make the necessary changes to your domain's DNS records within the `db.ngo.us` zone file. Ensure that any changes follow the correct format, including the use of proper TTL values and nameservers.

3. **Commit the Changes**:
   - Ensure that your commit is **signed**. You can do this by using `git commit -S` if you have set up GPG signing on your GitHub account.
   - In the commit message, clearly describe the changes you made (e.g., "Updated NS records for happycat.ngo.us").

4. **Submit a New Pull Request (PR)**:
   Push the changes to your fork and create a new pull request in the main repository. Be sure to provide all relevant details in the PR description, just as you did when you initially applied.

5. **Monitor and Review**:
   Ensure all checks pass and keep an eye on the PR for any requests for changes or updates from the maintainers. After approval, the changes will be merged, and your updates will propagate within 48 hours.

## Registrant Obligations

The ongoing trust and integrity of the `.ngo.us` registry depend on the accuracy and activity of its entries. By submitting a pull request to register a domain, the registrant agrees to the following obligations:

- **Maintain Eligibility**: The registrant commits to maintaining the eligibility of their organization and complying with the [terms of service](https://nic.ngo.us/terms-of-service/) at all times.
  
- **DNS Record Maintenance**: The registrant acknowledges their responsibility to regularly review and update their DNS records. This includes ensuring that all registered domains resolve correctly and that associated websites remain active.

- **Domain Removal**: Entries may be removed from the registry if:
  - The domain does not resolve in DNS.
  - The associated website becomes inactive.
  - The email address provided becomes unreachable.
  - Terms of service violation.

- **Up-to-date Contact Information**: Registrants must ensure that the email address provided in their section is always current and reachable. It is their responsibility to update this email address as necessary to continue receiving important communications and notices from the registry.

## Disclaimer

Please note that while `.ngo.us` is included in Mozilla's Public Suffix List (PSL), it is **not** an ICANN-accredited domain. The `.ngo.us` registry is not affiliated with the `.us` TLD registry or the Internet Corporation for Assigned Names and Numbers (ICANN). We operate independently as a community-driven registry. For more information on the PSL, visit [https://publicsuffix.org](https://publicsuffix.org). We believe in transparency, and hope this clarifies our independent status from official domain name regulatory bodies.

## Donations

If you find this service helpful for your nonprofit and wish to support us in maintaining and running this initiative, please consider [donating](https://ko-fi.com/fugue) to keep the service alive for others in the community!

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/O5O110ZK9B)

Thank you for choosing `.ngo.us` for your nonprofit's online presence!
