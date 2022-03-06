<script>
  import { marked } from 'marked';
  import { sanitize } from 'dompurify';

  let value = 'Some words are *italic*, some are **bold**, but all are sanitized!';
</script>

{@html sanitize(marked(value))}

<textarea bind:value={value}></textarea>

<style>
  textarea {
    max-width: 100%;
    width: 100%;
    height: 200px;
  }
</style>
