# Key Metrics for SRE and SLAs

## Key Metrics in SRE

In Site Reliability Engineering (SRE), we track a few important metrics:

1. **Service Level Indicators (SLIs)**: These are numbers that measure service quality. For example, how fast a page loads or how often a system crashes.

2. **Service Level Objectives (SLOs)**: These are goals we set for our SLIs. For example, we might aim to have our page load in under one second 99% of the time.

3. **Service Level Agreements (SLAs)**: These are promises we make to our users about our SLOs. For example, we might promise our users that our page will load in under one second 99% of the time, or we'll give them their money back.

4. **Error Budget**: This is how much our actual performance can differ from our SLO before we need to take action.

## SLAs of Two Big Companies

Let's look at two big companies, Google Cloud Platform (GCP) and Amazon Web Services (AWS):

1. **Google Cloud Platform (GCP)**: GCP promises that their Compute Engine will be available 99.95% of the time.

2. **Amazon Web Services (AWS)**: AWS makes the same promise for their EC2 and EBS services.

## Why These Metrics Are Important

These metrics help us make sure our services are reliable. They let us set goals (SLOs), make promises (SLAs), and figure out when we need to fix things (error budgets).
