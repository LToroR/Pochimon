[[_TOC_]]
import java.util.ArrayList;
public class Badge {
    private ArrayList<String> insignies;
    private String name;
    private String boost;
    private int obedienceLevel;

    public Badge(String name, String boost, int obedienceLevel) {
        this.name = name;
        this.boost = boost;
        this.obedienceLevel = obedienceLevel;
        this.insignies = new ArrayList<>();
    }
}

abstract class ElementAbs {
    protected String name;
    protected int XP;
    protected int level;
    protected int XPToLevelUp;

    public String getName() { 
    	return name; 
	}
    public void setName(String name) {
    	this.name = name; 
	}
    
    public int getXP() { 
    	return XP; 
    }
    public void setXP(int XP) { 
    	this.XP = XP; 
	}
    
    public int getLevel() {
    	return level; 
	}
    public void setLevel(int level) { 
    	this.level = level; 
    }
    
    public int getXPToLevelUp() { 
    	return XPToLevelUp; 
	}
    public void setXPToLevelUp(int XPToLevelUp) {
    	this.XPToLevelUp = XPToLevelUp; 
	}
}

public interface ICatchable {
	void tryToCatch();
    int getCaptureRate();
}

public class Move {
    private int id;
    private String name;
    private int powerPoints;
    private int maxPowerPoints;
    private Type type;

    public Move(int id, String name, int powerPoints, int maxPowerPoints, Type type) {
        this.id = id;
        this.name = name;
        this.powerPoints = powerPoints;
        this.maxPowerPoints = maxPowerPoints;
        this.type = type;
    }

    public void useMove() {
        if (powerPoints > 0) {
            powerPoints--;
        }
    }
}

public class Pochimon extends ElementAbs implements ICatchable {
    private Move move;
    private PochimonSpecies species;
    private Type type;

    public Pochimon(Move move, PochimonSpecies species, Type type) {
        this.move = move;
        this.species = species;
        this.type = type;
    }

    public void attackFoe() {}
    public void evolve() {}

    @Override
    public void tryToCatch() {}

    @Override
    public int getCaptureRate() { return 0; }
}

import java.util.ArrayList;
class PochimonSpecies {
    private String nameSpecie;
    private String specie;
    private ArrayList<Type> basicType;

    public PochimonSpecies(String nameSpecie, String specie, ArrayList<Type> basicType) {
        this.nameSpecie = nameSpecie;
        this.specie = specie;
        this.basicType = basicType;
    }

    public ArrayList<Type> getBasicType() { return basicType; }
}

import java.util.ArrayList;
public class Trainer extends ElementAbs {
    private ArrayList<Badge> badges;

    public Trainer() {
        this.badges = new ArrayList<>();
    }

    public void organizeInsignies() {}
}

import java.util.ArrayList;
public class Type {
    private TypeEnum type;
    private ArrayList<TypeEnum> effectiveAgainst;
    private ArrayList<TypeEnum> weakAgainst;

    public Type(TypeEnum type) {
        this.type = type;
        this.effectiveAgainst = new ArrayList<>();
        this.weakAgainst = new ArrayList<>();
    }

    public TypeEnum getType() { 
    	return type; 
    }
    public ArrayList<TypeEnum> getEffectiveAgainst() {
    	return effectiveAgainst; 
    }
    public ArrayList<TypeEnum> getWeakAgainst() { 
    	return weakAgainst; 
    }
}

public enum TypeEnum {
    FIRE, WATER, GRASS, ROCK, STEEL, POISON, SINESTER, DARK, FAIRY, ELECTRIC, NORMAL, FIGHT;
}

## Sobre el projecte

Aquest projecte és una implementació de *Pochimon*.

## Contacte
**Lucas Toroo** - ***ltoro@ibadia.cat***.

Enllaç del projecte:
[https://github.com/user/pochimon](https://github.com/user/pochimon)