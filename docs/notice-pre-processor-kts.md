# The `notice-pre-processor.kts` file

The `notice-pre-processor.kts` file enables customization of the generated open source notices
such as headers, footers and the conditional inclusion of a source code offer.

You can use the [notice-pre-processor.kts example](../examples/notice-pre-processor.kts) as the base script file to
create your custom open source notices.

## Command Line

To use the `notice-pre-processor.kts` file pass it to the `preProcessingScript` option of the _NoticeByPackage_ and _NoticeSummary_ reporters:

```bash
cli/build/install/ort/bin/ort report
  -i [evaluator-output-dir]/evaluation-result.yml
  -o [reporter-output-dir]
  --report-formats NoticeByPackage,StaticHtml,WebApp
  -O NoticeByPackage=preProcessingScript=$ORT_CONFIG_DIR/notice-pre-processor.kts \
  -O NoticeSummary=preProcessingScript=$ORT_CONFIG_DIR/notice-pre-processor.kts \
```
