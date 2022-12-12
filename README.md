# betarelics
a slay the spire mod which adds back some older art for relics to the game.


also lets you add your own beta art to relics from your own mod.
example:
```java
public class AwesomeRelic extends CustomRelic {
    public static String ID = "AwesomeMod:AwesomeRelic";

    public static String IMG_PATH = "AwesomeResources/relics/Awesome.png";
    public static String IMG_BETA_PATH = "AwesomeResources/relics/AwesomeBeta.png";
    public static String OUTLINE_IMG_PATH = "AwesomeResources/relics/outline/Awesome.png";
    public static String OUTLINE_BETA_IMG_PATH = "AwesomeResources/relics/outline/AwesomeBeta.png";
    public static String LARGE_IMG_PATH = "AwesomeResources/relics/AwesomeLarge.png";
    public static String LARGE_BETA_IMG_PATH = "AwesomeResources/relics/AwesomeLargeBeta.png";

    static {
        if (Loader.isModLoaded("betarelics"))
            BetaRelics.register(ID, IMG_BETA_PATH, OUTLINE_BETA_IMG_PATH, LARGE_BETA_IMG_PATH);
    }

    public AwesomeRelic() {
        super(ID, ImageMaster.loadImage(IMG_PATH), ImageMaster.loadImage(OUTLINE_IMG_PATH), RelicTier.RARE, LandingSound.CLINK);
        this.largeImg = ImageMaster.loadImage(LARGE_IMG_PATH);
    }
}
```