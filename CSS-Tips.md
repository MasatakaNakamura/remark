
# Image on right, text on left

The following CSS creates a slide which has an image on the right and some text on the left. 

```
    .left-side {
    width: 40%;
    float: left;
    font-size: 75%
    }

    .right-side {
    width: 55%;
    float: right;
    }
      
    .right-side-wrap {
    width:100%;
    padding: 10% 5% 10% 5%;
      }

    .right-side-wrap img {
    border:5px solid lightgrey;
    width: auto;
    max-width: 95%;
    height: auto;
    max-height: 95%;
      }
```

To use this code, the img tag needs to be embedded in both .right-side and .right-side-wrap, as follows: `.right-side[.right-side-wrap[![title](./img/IMAGE.jpg)`