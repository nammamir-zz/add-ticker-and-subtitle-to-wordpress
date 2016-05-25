# Add Ticker and Subtitle to Wordpress pages and posts
This instruction shows you how to add Ticker and Subtitle to Wordpress posts and/or pages

<ol>
  <li>Find the title of the post/page on the code of the theme (mostly located in the file <code>index.php</code>)<br>
  For this reason you need to look for something like <code><?php the_title();?></code> or <code><?php single_post_title();?></code></li>
  <li>Add the following code to the file (here index.php), exactly before the title as the Ticker:
  <code>
  <?php $Ticker_value = get_post_meta( get_the_ID(), 'Ticker', true ); if( ! empty( $Ticker_value ) ) { echo $Ticker_value; } ?></code>
  </li>
  <li>Add the following code to the file (here index.php), exactly after the title as the Subtitle:
  <code>
  <?php
    Subtitle_value = get_post_meta( get_the_ID(), 'Subtitle', true ); 
    if( ! empty( $Subtitle_value ) ) 
      { echo $Subtitle_value; }
  ?></code>
  </li>
  <li>Now, you just need to use "Custome Fileds" to have these two features in your post/page:
    <ul>
      <li>Ticker</li>
      <li>Subtitle</li>
    </ul>
</ol>
