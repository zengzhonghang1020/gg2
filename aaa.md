aaa.md```plantuml
@startuml

package reactor.core {
    class ReactorDemo8 {
        + main(args: String[]): void
    }

    class DishFactory {
        + createDishesFlux(dishes: List<String>): Flux<String>
    }

    class DishPreparationService {
        + prepareDish(dishesFlux: Flux<String>): Flux<String>
    }

    class DishAvailabilityFilter {
        + isAvailable(dish: String): boolean
    }

    class DishOrderService {
        + orderDish(dish: String): Mono<String>
        + wordprint(dish: String): Mono<String>
    }
}

@enduml
