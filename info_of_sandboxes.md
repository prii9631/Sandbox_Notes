What is salesforce sandbox?

1.A salesforce sandbox is an isolated copy of your production
environment that allows teams to safely test changes,
new features and code without risking live data.
2.These replicas enabling you to plan, build, test,
deploy and train users without affecting your production
environment.

**Key Benefits**

① Risk Reduction ⇒ Test changes without impacting production data or business operations.

② Safe Development ⇒ Develop customizations, configurations
and apps in isolation.

③ User Training ⇒ Provide realistic training environment
without affecting the data.

④ compliance ⇒ Protect sensitive production data while
enabling through thorough testing.

**Type of sandboxes**

There are four types

① Developer Sandbox ::
The most basic testing environment that only contains metadata and a minimal amount of other
information, making it ideal for light weight development
and testing

① Data storage = 200 MB
② file storage = 200 MB
③ Refresh interval = Daily
④ Data included = Metadata only ( No production data )
⑤ cost = free with most salesforce licenses.

Best for ⇒

① individual developer testing
② code development and debugging
③ Trial and error testing for new features
④ practice environment for new users
⑤ simple customization testing

② Developer Pro sandbox ⇒
Overview: A specialized environment that supports more extensive development and testing activities than the standard Developer Sandbox, with increased storage capacity.

**Specifications **:

• Data Storage: 1 GB
• File Storage: 1 GB
• Refresh Interval: Daily (once per day)
• Data Included: Metadata only (reports, dashboards, price books, products, apps, customizations)
• Availability: Included with Unlimited and Performance editions, can be purchased separately

Best For:

• Larger development projects
• Teams requiring more storage
• Integration testing
• User training with enhanced storage needs

3. Partial Copy Sandbox
   Overview: Includes all of your organization's metadata and adds a selected amount of your production organization's data that you define using a sandbox template.

Specifications:

• Data Storage: Up to 5 GB of data
• File Storage: Matches production org
• Record Limit: Maximum of 10,000 records per selected object
• Refresh Interval: Every 5 days
• Data Included: All metadata + selected production data via templates
• Availability: Enterprise, Unlimited, and Performance editions

Best For:
• User acceptance testing (UAT)
• Integration testing with realistic data
• Training users with real-world data
• Testing with representative data subsets
• QA processes requiring actual data

4. Full Copy Sandbox
Overview: A complete replica of your production environment, encompassing all metadata, data, and files. This sandbox type provides the most accurate testing environment.

Specifications:

• Data Storage: Complete production data unlimited, matches product
• File Storage: Matches production org
• Refresh Interval Every 20 days
• Data Included: All metadata, data, records, documents, and attachments
• Availability: Unlimited and Performance editions lone included), can be purchased separately

Best For:
• Performance and load testing
• Pre-deployment staging
• Complete user acceptance testing
• Deta migration testing
• Full system integration testing
• Firual testing before production deployment
