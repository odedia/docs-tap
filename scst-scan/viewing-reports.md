# Viewing Vulnerability Results

After completing the scans, query the [Supply Chain Security Tools - Store](../scst-store/overview.md) to view your vulnerability results. The Supply Chain Security Tools - Store is a Tanzu component that stores image, package, and vulnerability metadata about your dependencies. Use the Supply Chain Security Tools - Store CLI, called `insight`, to query metadata that is submitted to the store.

For example, to query Vulnerability data relating to an Image Scan, run:
```bash
# Query for image scans:
kubectl get imagescans

# and grab the sha256 digest and replace in the following example query:
insight image get \
  --digest sha256:06ba459dc32475871646f22c980d5db4335021d76e1693c8a87bf02aed8c1a3e \
  --format json
```

> **NOTE:** You must have the [Supply Chain Security Tools - Store prerequisites](../scst-store/using_metadata_store.md) for the example to run successfully.

For a complete guide on how to query the store, see [Querying Supply Chain Security Tools - Store](../scst-store/querying_the_metadata_store.md).