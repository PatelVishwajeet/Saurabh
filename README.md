public class Plant {
    private String name;
    private int waterRequirement; // in milliliters
    private int currentWaterLevel; // in milliliters

    public Plant(String name, int waterRequirement) {
        this.name = name;
        this.waterRequirement = waterRequirement;
        this.currentWaterLevel = 0; // initially no water
    }

    public String getName() {
        return name;
    }

    public int getWaterRequirement() {
        return waterRequirement;
    }

    public int getCurrentWaterLevel() {
        return currentWaterLevel;
    }

    public void water(int amount) {
        currentWaterLevel += amount;
        if (currentWaterLevel > waterRequirement) {
            currentWaterLevel = waterRequirement; // cap the water level
        }
    }

    public boolean needsWater() {
        return currentWaterLevel < waterRequirement;
    }
}
