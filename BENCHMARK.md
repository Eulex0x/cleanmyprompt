# Clean My Prompt - Benchmark Test Text

Use this text to test the sanitization features. Click "Load Test Benchmark" in the app or copy-paste below:

---

Dear Team,

I hope this email finds you well. I'm John Smith, Senior Software Engineer at Microsoft Corporation, and I'm reaching out regarding our upcoming project collaboration.

Contact Information:
- Email: john.smith@microsoft.com
- Personal: jsmith1985@gmail.com
- Phone: (555) 123-4567
- Office: +1-206-555-9876

Our team is based in Seattle, Washington, and we're working with several partners:
- Sarah Johnson from Google in Mountain View, California
- Dr. Michael Chen from Amazon Web Services in Portland, Oregon
- Emily Rodriguez at Apple Inc. in Cupertino

Project Details:
API Keys for development:
- Primary: sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
- Backup: api_key_prod_xxxxxxxxxxxxxxxxxxxx

Database Credentials:
- Server: db.internal.company.com (IP: 192.168.1.100)
- Backup: 10.0.0.50
- Production: 172.16.0.25

Payment Information (for vendor setup):
Credit Card: 4532-1234-5678-9010
Expiration: 12/2025
CVV: 123

Additional team members:
- Robert Williams (robert.w@techstart.io) from TechStart Inc.
- Jennifer Davis working at IBM in New York City
- David Martinez from Oracle Corporation

Please let me know if you need any additional information. You can reach me at my secondary email: john.personal@outlook.com or call my mobile: 555-987-6543.

Looking forward to collaborating with you all!

Best regards,
John Smith
Senior Software Engineer
Microsoft Corporation
Seattle, WA 98101

---

## Expected Detections:

**With Smart NLP + Realistic Mode ON:**
- **Names**: John Smith, Sarah Johnson, Dr. Michael Chen, Emily Rodriguez, Robert Williams, Jennifer Davis, David Martinez, Max Müller, Sophie Martin
- **Companies**: Microsoft Corporation, Google, Amazon Web Services, Apple Inc., SAP, Airbus, TechStart Inc., IBM, Oracle Corporation
- **Locations**: Seattle, Washington, Mountain View, California, Portland, Oregon, Cupertino, Walldorf, Germany, Toulouse, France, London, UK, Stuttgart, Munich, Bavaria
- **Emails**: 5 email addresses
- **Phones**: 8 phone numbers (US + German + EU formats)
- **API Keys**: 4 keys (GitHub, Stripe, AWS, generic)
- **IP Addresses**: 4 IPs (3 IPv4 + 1 IPv6)
- **URLs**: 3 web addresses
- **Credit Cards**: 1 card number
- **IBANs**: 2 European bank accounts
- **Postal Codes**: 3 codes (US, UK, German)
- **Credentials**: 2 username/password pairs

**Total**: 60+ sensitive items detected across US and EU formats
