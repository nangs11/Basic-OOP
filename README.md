# Marketing Data ETL Project

This project contains classes for Extract, Transform, and Load (ETL) processes for marketing data.

## MarketingDataETL Class

The `MarketingDataETL` class provides methods to extract, transform, and store marketing data from a CSV file.

### Methods

1. `extract()`: Extracts data from a CSV file specified by the `file_path`.
2. `transform()`: Cleans and transforms the extracted data.
3. `store(output_file)`: Stores the transformed data into a CSV file specified by `output_file`.

## TargetedMarketingETL Class

The `TargetedMarketingETL` class inherits from `MarketingDataETL` and extends it with additional functionality for customer segmentation.

### Additional Method

1. `segment_customers(criteria)`: Segments customers based on specified criteria such as total spent or product category.

### Overridden Method

The `transform()` method is overridden to include customer segmentation logic in addition to the standard data transformation process.

## Example Usage

```python
if __name__ == "__main__":
    # Example usage of MarketingDataETL
    etl = MarketingDataETL("marketing_data.csv")
    etl.extract()
    etl.transform()
    etl.store("transformed_marketing_data.csv")

    # Example usage of TargetedMarketingETL
    targeted_etl = TargetedMarketingETL("marketing_data.csv")
    targeted_etl.extract()
    targeted_etl.transform()
    targeted_etl.segment_customers('product_category')
