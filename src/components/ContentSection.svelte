<script>
  import FaFacebook from "svelte-icons/fa/FaFacebook.svelte";
  import FaTwitter from "svelte-icons/fa/FaTwitter.svelte";
  import FaGooglePlusSquare from "svelte-icons/fa/FaGooglePlusSquare.svelte";
</script>

<style lang="scss">
  .wrapper {
    margin: 10px auto;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .left {
    max-width: 500px;
    margin: 0 auto;
    h1 {
      color: darkslateblue;
    }
  }
  .blog-post {
    width: 80%;
    margin: 0 auto;
    padding: 20px;
    .image {
      width: 100%;
      height: auto;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 10px;
      }
    }
    .post-desc {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      .desc-left {
        width: 100%;
        span {
          color: darkslateblue;
          cursor: pointer;
        }
      }
      .desc-right {
        width: 100%;
      }
    }
  }
  .right {
    max-width: 500px;
    margin: 0 auto;
    .search {
      width: 100%;
      input {
        width: 100%;
      }
    }
    .icons {
      width: 80%;
      margin: 20px;
      display: flex;
      justify-content: space-around;

      .icon {
        width: 40px;
        height: 40px;
      }
      .f,
      .t,
      .g {
        cursor: pointer;
      }
      .f {
        color: #3b5998;
      }
      .t {
        color: #00acee;
      }
      .g {
        color: #ea4335;
      }
    }

    .subscribe {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      input {
        width: 100%;
      }
      button {
        background-color: crimson;
        color: white;
        width: 200px;
        height: 50px;
        border: 2px solid crimson;
        font-size: 20px;
        margin: 10px 0px;
        font-weight: bold;
        &:hover {
          background-color: white;
          color: crimson;
          cursor: pointer;
          transition-property: background-color, color;
          transition-duration: 0.3s;
        }
      }
    }
    .categories {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      h1 {
        color: grey;
      }
      p::before {
        content: "";
        width: 0px;
        height: 0px;
        border-style: solid;
        border-width: 10px 15px 10px 0;
        border-color: transparent crimson transparent transparent;
        display: inline-block;
        vertical-align: middle;
        margin-right: 5px;
        transform: rotate(180deg) scale(0.8);
      }
    }
    .recent-posts {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      h1 {
        color: grey;
      }
      p {
        color: grey;
        font-weight: bold;
      }
    }
    .tags {
      h1 {
        color: grey;
      }
      .tags-wrapper {
        display: flex;
        flex-wrap: wrap;
        .tag {
          background: #f2f2f2;
          width: fit-content;
          height: fit-content;
          margin: 5px;
          padding: 5px 15px;
          &:hover {
            background-color: crimson;
            transition: background-color 0.3s;
            p {
              color: white;
            }
          }
          p {
            color: grey;
            padding: 0;
            margin: 0;
          }
        }
      }
    }
  }
  @media (min-width: 960px) {
    .wrapper {
      max-width: 1160px;
      margin: 50px auto;
      padding: 50px;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }
    .left {
      width: 65%;
      h1 {
        color: darkslateblue;
      }
    }
    .blog-post {
      width: 80%;
      padding: 20px;
      .image {
        width: 100%;
        height: auto;
        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          border-radius: 10px;
        }
      }
      .post-desc {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        .desc-left {
          width: 50%;
          span {
            color: darkslateblue;
            cursor: pointer;
          }
        }
        .desc-right {
          width: 50%;
        }
      }
    }
    .right {
      width: 35%;
      .search {
        width: 100%;
        input {
          width: 100%;
        }
      }
      .icons {
        width: 80%;
        margin: 20px;
        display: flex;
        justify-content: space-around;

        .icon {
          width: 40px;
          height: 40px;
        }
        .f,
        .t,
        .g {
          cursor: pointer;
        }
        .f {
          color: #3b5998;
        }
        .t {
          color: #00acee;
        }
        .g {
          color: #ea4335;
        }
      }

      .subscribe {
        display: block;
        width: 100%;
        input {
          width: 100%;
        }
        button {
          background-color: crimson;
          color: white;
          width: 200px;
          height: 50px;
          border: 2px solid crimson;
          font-size: 20px;
          margin: 10px 0px;
          font-weight: bold;
          &:hover {
            background-color: white;
            color: crimson;
            cursor: pointer;
            transition-property: background-color, color;
            transition-duration: 0.3s;
          }
        }
      }
      .categories {
        display: block;
        h1 {
          color: grey;
        }
        p::before {
          content: "";
          width: 0px;
          height: 0px;
          border-style: solid;
          border-width: 10px 15px 10px 0;
          border-color: transparent crimson transparent transparent;
          display: inline-block;
          vertical-align: middle;
          margin-right: 5px;
          transform: rotate(180deg) scale(0.8);
        }
      }
      .recent-posts {
        display: block;
        h1 {
          color: grey;
        }
        p {
          color: grey;
          font-weight: bold;
        }
      }
      .tags {
        h1 {
          color: grey;
        }
        .tags-wrapper {
          display: flex;
          flex-wrap: wrap;
          .tag {
            background: #f2f2f2;
            width: fit-content;
            height: fit-content;
            margin: 5px;
            padding: 5px 15px;
            &:hover {
              background-color: crimson;
              transition: background-color 0.3s;
              p {
                color: white;
              }
            }
            p {
              color: grey;
              padding: 0;
              margin: 0;
            }
          }
        }
      }
    }
  }
</style>

<div class="wrapper">
  <div class="left">
    <h1>Lorem ipsum dolor sit amet</h1>
    <div class="blog-post">
      <div class="image"><img src="assets/laptop1.jpg" alt="l1" /></div>
      <div class="post-desc">
        <div class="desc-left">
          <p>Posted on March 24, 2019</p>
          <p>Tags: <span>Website | Design</span></p>
          <p>Comments: 8</p>
        </div>
        <div class="desc-right">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Eu sem
          integer vitae justo eget magna fermentum iaculis.
        </div>
      </div>
    </div>
    <div class="blog-post">
      <div class="image"><img src="assets/laptop2.jpg" alt="l2" /></div>
      <div class="post-desc">
        <div class="desc-left">
          <p>Posted on January 14, 2020</p>
          <p>Tags: <span>Website | Design</span></p>
          <p>Comments: 8</p>
        </div>
        <div class="desc-right">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Eu sem
          integer vitae justo eget magna fermentum iaculis.
        </div>
      </div>
    </div>
  </div>
  <div class="right">
    <div class="search"><input placeholder="Search" /></div>
    <h1>Follow Us</h1>
    <div class="icons">
      <div class="icon f">
        <FaFacebook />
      </div>
      <div class="icon t">
        <FaTwitter />
      </div>
      <div class="icon g">
        <FaGooglePlusSquare />
      </div>
    </div>
    <div class="subscribe">
      <input placeholder="Enter Your e-mail" /><button>Subscribe</button>
    </div>
    <div class="categories">
      <h1>Categories</h1>
      <p>Lorem ipsum dolor sit</p>
      <p>Lorem ipsum dolor sit</p>
      <p>Lorem ipsum dolor sit</p>
    </div>
    <div class="recent-posts">
      <h1>Recent posts</h1>
      <p>Lorem ipsum dolor sit</p>
      <p>Lorem ipsum dolor sit</p>
      <p>Lorem ipsum dolor sit</p>
    </div>
    <div class="tags">
      <h1>Tags</h1>
      <div class="tags-wrapper">
        <div class="tag">
          <p>Lorem</p>
        </div>
        <div class="tag">
          <p>ipsum</p>
        </div>
        <div class="tag">
          <p>dolor</p>
        </div>
        <div class="tag">
          <p>sit</p>
        </div>
        <div class="tag">
          <p>amet</p>
        </div>
        <div class="tag">
          <p>consectetur</p>
        </div>
        <div class="tag">
          <p>elit</p>
        </div>
        <div class="tag">
          <p>adipiscing</p>
        </div>
        <div class="tag">
          <p>sed</p>
        </div>
        <div class="tag">
          <p>do</p>
        </div>
      </div>
    </div>
  </div>
</div>
