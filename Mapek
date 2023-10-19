import java.util.*;

public class Runner {
    public static void main(String[] args) {

        System.out.println("hashmap");
        HashMap<Building, ArrayList<Room>> hashMap = new HashMap<>();

        ArrayList<Room> rooms = new ArrayList<>();
        rooms.add(new Room(new Building("DEIK", "Kassai u. 26."), "F01"));
        rooms.add(new Room(new Building("deik", "Kassai u. 26."), "F0"));
        rooms.add(new Room(new Building("DEIK", "Kassai u. 26."), "206"));
        rooms.add(new Room(new Building("DEIK", "Kassai u. 26."), "310"));
        rooms.add(new Room(new Building("Foepulet", "Egyetem ter 1."), "Aud Max"));
        rooms.add(new Room(new Building("Foepulet", "Egyetem ter 1."), "Romai 1"));
        rooms.add(new Room(new Building("Kemia", "Egyetem ter 1."), "K1"));

        for (Room room: rooms) {
            ArrayList<Room> ertek;
            if (hashMap.containsKey(room.getBuilding())) {
                ertek = hashMap.get(room.getBuilding());
            }
            else {
                ertek = new ArrayList<>();
            }
            ertek.add(room);
            hashMap.put(room.getBuilding(), ertek);
        }

        for (Map.Entry<Building, ArrayList<Room>> entry: hashMap.entrySet()) {
            Building building = entry.getKey();
            ArrayList<Room> roomArrayList = entry.getValue();

            System.out.println(building);
            System.out.println(roomArrayList);
            System.out.println("-----");
        }

        System.out.println("treemap");

//        TreeMap<Building, ArrayList<Room>> treeMap = new TreeMap<>();
        TreeMap<Building, ArrayList<Room>> treeMap = new TreeMap<>(new Comparator<Building>() {
            @Override
            public int compare(Building o1, Building o2) {
                return o2.getName().toLowerCase().compareTo(o1.getName().toLowerCase());
            }
        });

        for (Room room: rooms) {
            ArrayList<Room> roomArrayList;
            if (treeMap.containsKey(room.getBuilding())) {
                roomArrayList = treeMap.get(room.getBuilding());
            }
            else {
                roomArrayList = new ArrayList<>();
            }
            roomArrayList.add(room);
            treeMap.put(room.getBuilding(), roomArrayList);
        }

        for (Map.Entry<Building, ArrayList<Room>> entry: treeMap.entrySet()) {
            Building building = entry.getKey();
            ArrayList<Room> roomArrayList = entry.getValue();

            System.out.println(building);
            System.out.println(roomArrayList);
            System.out.println("-----");
        }

    }

}
