[[_TOC_]]

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

## Sobre el projecte

Aquest projecte és una implementació de *Pochimon*.

## Contacte
**Lucas** - ***ltoro@ibadia.cat***

Enllaç del projecte:
[https://github.com/user/pochimon](https://github.com/user/pochimon)