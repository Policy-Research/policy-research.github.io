// =============================================================================
// Data Grid - Usage
// =============================================================================

// Version:         1.0.0


// #DG.create()         
// -----------------------------------------------------------------------------
//    Description:                      Used to add a grid to the site, 
//                                      this is the base of a new grid.
//                                      Most arguments can be omitted, but optional
//                                      arguments will allow you to make a custom
//                                      grid with a different attribute names.
//                                      Although most times it would be more useful to 
//                                      modify the default variables for the module.
//    Parameters:
//      @columns:              [number] Number of columns
//      @breakpoint       [media query] The media query when the grid is active, 
//                                      upwards only, for example if you wanted 
//                                      the grid to start above table size, you 
//                                      would pass @table-up.
//      @gutter            [unit/pixel] The size of the gutter (must be divisible by 2)
//      @attr                  [string] The parent attribute for the grid, only 
//                                      change if needed because of naming conflict.
//                                      Also consider changing the default for data-grid 
//                                      if the issue is because of a naming conflict.
//      @optional             [ruleset] Wrap related modifier mixins (breakpoint, rules)
//                                      in a detached ruleset for output in the scope of 
//                                      the grid.

// breakpoint()         
// -----------------------------------------------------------------------------
//    Description:                      This function is used to generate another
//                                      breakpoint for your grid. You could use the 
//                                      .create() function to create new breakpoints
//                                      but it would duplicate unneeded CSS. This 
//                                      will generate only what is needed for a 
//                                      breakpoint.
//
//                                      Note: Order your breakpoints from 
//                                            smallest -to- largest. The grid relies 
//                                            on media queries overriding.
//    Parameters:
//      @suffix:               [number] This is the string used to discern from default 
//                                      property names. In the example below the string 
//                                      "large" is the suffix added to all grid properties. 
//                                      Properties like width and offset. 
//                                        <el data-grid-item="width: 3, width-large: 1">
//                                        </el>
//      @columns:              [number] Should match grid settings you passed to 
//                                      create() the grid
//      @breakpoint       [media query] The media query that this breakpoint will 
//                                      begin to apply, use upwards media queries only!
//      @gutter            [unit/pixel] The size of the gutter for this breakpoint, 
//                                      must be divisible by 2.
//      @attr                  [string] Should match grid settings you passed to 
//                                      create() the grid
// 

// ruleStyle()         
// -----------------------------------------------------------------------------
//    Description:                      Creates a new style of rules for the grid.
//                                      For example a thicker rule, or a rule of 
//                                      a different color.
// 
//    Parameters:
//      @style                 [string] The name of the new style. This will be 
//                                      matched to the rules-column-style and
//                                      rules-row-style.
//      @size              [unit/pixel] Size in pixels for the rule
//      @color                 [string] Color to apply to the rule