# Enemy AI System Tutorial

This tutorial shows how to create an easily expandable AI enemy system in Unity.

## 1. Setup

Import the `AI Navigation` package via the package manager window

Create a cylinder to act as the enemy, this can always be changed later.

Create a layer called `Enemy` and apply it to your enemy object.

Next create an empty gameobject in the scene and call it `NavMesh`, on this object apply the `NavMeshSurface` component and bake the scene.

Now on the enemy object apply the `Nav Mesh Agent` component, the default values are fine.

## 2. Create AI Script

Under your scripts folder create a new script and call it `EnemyAI`

### Refrences

In this script we need to create the variales to control the properties of the AI:

```.cs
    public NavMeshAgent agent;
    public Transform player;
    public LayerMask whatIsGround, whatIsPlayer;
    public float health;
    public Vector3 walkPoint;
    bool walkPointSet;
    public float walkPointRange;
    public float timeBetweenAttacks;
    bool alreadyAttacked;
    public GameObject projectile;
    public float sightRange, attackRange;
    public bool playerInSightRange, playerInAttackRange;
```