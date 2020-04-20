<script>
export default {
  name: "CarbonAds",
  watch: {
    $route(to, from) {
      if (
        to.path !== from.path &&
        // Only reload if the ad has been loaded
        // otherwise it's possible that the script is appended but
        // the ads are not loaded yet. This would result in duplicated ads.
        this.$el.querySelector("#carbonads")
      ) {
        this.$el.innerHTML = "";
        this.load();
      }
    }
  },
  mounted() {
    if (process.env.NODE_ENV === "production") {
      this.load();
    }
  },
  methods: {
    load() {
      const caServe = this.$site.themeConfig.carbonAds.serve;
      const caPlacement = this.$site.themeConfig.carbonAds.placement;
      const script = document.createElement("script");
      script.id = "_carbonads_js";
      script.src = `//cdn.carbonads.com/carbon.js?serve=${caServe}&placement=${caPlacement}`;
      this.$el.appendChild(script);
    }
  },
  render(h) {
    return h("div", { class: "carbon-ads" });
  }
};
</script>

<style lang="stylus">
.carbon-ads {
  min-height: 102px;
  padding: 1.5rem 1.5rem 0;
  margin-bottom: -0.5rem;
  font-size: 0.75rem;

  a {
    color: #444;
    font-weight: normal;
    display: inline;
  }

  .carbon-img {
    float: left;
    margin-right: 1rem;
    border: 1px solid $borderColor;

    img {
      display: block;
    }
  }

  .carbon-poweredby {
    color: #999;
    display: block;
    margin-top: 0.5em;
  }
}

@media (max-width: $MQMobile) {
  .carbon-ads {
    .carbon-img img {
      width: 100px;
      height: 77px;
    }
  }
}
</style>
